% Nodes Creation (node location)

% Set Max Grid value of X,Y,Z (divide by 2 for each axis value)
% if GrainId is 144X133X133, then each max Value will be 144/2,133/2,133/2
xMax = 179/2;
yMax = 174/2;
zMax = 136/2;

% Set the space : space defines the size of each element
space = 0.5

xGrid = 0:space:xMax
yGrid = 0:space:yMax
zGrid = 0:space:zMax

% Calculate the number of nodes
nodesNum = length(xGrid)*length(yGrid)*length(zGrid);


% Create Matrix for nodes data input
nodesMatrix = zeros(nodesNum,4);

% Nodes numbering in Matrix
nodesMatrix(:,1) = 1:nodesNum;


% Set data for input (every location of nodes)
xNodes = repmat(xGrid,1,length(yGrid)*length(zGrid));
xNodes = xNodes(:);

yNodes = repmat(yGrid,length(xGrid),length(zGrid));
yNodes = yNodes(:);

zNodes = repmat(zGrid,length(xGrid)*length(yGrid),1);
zNodes = zNodes(:);

% Input data in Matrix
nodesMatrix(:,2) = xNodes;
nodesMatrix(:,3) = yNodes;
nodesMatrix(:,4) = zNodes;


% Result of node matrix
nodesMatrix
nodesMatrixForSave = zeros(nodesNum*4,1);
nodesMatrixForSave(1:4) = nodesMatrix(1,:);
for i = 1:nodesNum
    nodesMatrixForSave((i*4)+1:(i*4)+4) = nodesMatrix(i,:);
end

nodesMatrixForSave




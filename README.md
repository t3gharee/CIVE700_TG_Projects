# CIVE700_TG_Projects
here you'll find CIVE700 Projects prepared by me
function your_cards1 = your_cards()
% This function create matrix 4X13 of all cards, simulate hand of randomly selected seven cards and identify the locations of those seven cards on the matrix of all cards.
all_cards=zeros(4,13);
your_cards1=zeros(4,13);
all_cards(:,1)=[1 2 3 4]';
for ii=2:13
    all_cards(:,ii)=all_cards(:,ii-1)+4;
end
your_cards=randperm(52,7); % simulate a hand of randomly selected seven cards
%%%%%% The next line for the purpose of manual test only
%%your_cards=[29 46 6 14 52 38 22]; % manual test
hand1=zeros(7,2);
for ii=1:7
    [s r]  =find(all_cards==your_cards(ii));
    hand1(ii,:)=[s r]'; % identify the locations of those seven cards on the matrix of all cards as (row, column)
end
your_cards
for ii=1:7
    your_cards1(hand1(ii,1),hand1(ii,2))=1; % create a new 4X13 matrix of zeros except the locations of hand cards are identified with ones
end
end

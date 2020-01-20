# CIVE700_TG_Projects
**Code**
Code block


1. here you'll find CIVE700 Projects prepared by me
2. function your_cards1 = your_cards()
3. % This function create matrix 4X13 of all cards, simulate hand of randomly selected seven cards and identify the locations of those seven cards on the matrix of all cards.
4. all_cards=zeros(4,13);
5. your_cards1=zeros(4,13);
6. all_cards(:,1)=[1 2 3 4]';
7. for ii=2:13
8.     all_cards(:,ii)=all_cards(:,ii-1)+4;
9. end
10. your_cards=randperm(52,7); % simulate a hand of randomly selected seven cards
11. %%%%%% The next line for the purpose of manual test only
12. %%your_cards=[29 46 6 14 52 38 22]; % manual test
13. hand1=zeros(7,2);
14. for ii=1:7
15.    [s r]  =find(all_cards==your_cards(ii));
16.     hand1(ii,:)=[s r]'; % identify the locations of those seven cards on the matrix of all cards as (row, column)
17. end
18. your_cards
19. for ii=1:7
20.     your_cards1(hand1(ii,1),hand1(ii,2))=1; % create a new 4X13 matrix of zeros except the locations of hand cards are identified with ones
21. end
22. end
[***course website***](https://github.com/chulminy/CIVE497-CIVE700) 	

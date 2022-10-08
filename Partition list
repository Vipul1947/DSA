/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode() : val(0), next(nullptr) {}
 *     ListNode(int x) : val(x), next(nullptr) {}
 *     ListNode(int x, ListNode *next) : val(x), next(next) {}
 * };
 */
class Solution {
public:
    
    ListNode* partition(ListNode* head, int x) {
        
        ListNode *glh=NULL;
        
        ListNode *slh=NULL;
        ListNode *glt=NULL;
        ListNode *slt=NULL;
        while(head!=NULL)
        {
            if(head->val>=x)
            {
                if(glh==NULL)
                {
                    glh=head;
                    glt=head;   
                }
                else
                {
                    glt->next=head;
                    glt=head;
                }
                
            }
            else
            {
                if(slh==NULL)
                {
                    slh=head;
                    slt=head;
                }
                else
                {
                    slt->next=head;
                    slt=head;
                }
            }
            head=head->next;
        }
        if(slt)
        slt->next=glh;
        if(glt)
        glt->next=NULL;
        if(slh)
        return slh;
        
        return glh;
    }
};

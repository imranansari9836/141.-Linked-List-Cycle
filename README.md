public class Solution {
    public boolean hasCycle(ListNode head) {
        ListNode fast=head;
        ListNode slow=head;
        while(fast!=null&& fast.next!=null)
        {
            fast=fast.next.next;//2x jump
            slow=slow.next;//1x jump
            if(fast==slow)//2x==1x
            {
                return true;//
            }
        }
        return false;
    }
}

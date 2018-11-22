<template>
    <div class='comment'>
		<span class='comment-author'>{{comment.author}}:</span>
        <span class='comment-content'>{{comment.content}}</span>
		<el-button style="margin-left:auto" @click.prevent='deleteMe' type="danger" icon="el-icon-delete" circle></el-button>
	</div>
</template>

<script>
 export default {
     props: ['comment'],
     methods: {
         deleteMe() {
             this.$emit('shanchuwo', this.comment.id);
         }
     }
 };
</script>

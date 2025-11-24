# phony targets are targets that don't actually create a file
.phony: deploy

# anvil's third default address
sender := 0x575483b681bdb31ae146aa3fe3f307b83cee557fc0432e5590787ebaf1e639ac
RPC_URL := https://lb.drpc.live/base/AhtRu-KKvEqhltBPZfL2v7C9YuMRwC0R8JHqQmlfqV1j

# deploying the contract
deploy:
	@PRIVATE_KEY=$(sender) forge script script/Deploy.s.sol:Deploy --broadcast --rpc-url $(RPC_URL)

# calling sayGM()
call-contract:
	@PRIVATE_KEY=$(sender) forge script script/CallContract.s.sol:CallContract --broadcast --rpc-url $(RPC_URL)

# Solidity Interface

## Factory Interface

```javascript
contract FactoryInterface() {
    // Public Variables
    address public exchangeTemplate;
    uint256 public tokenCount;
    // Create Exchange
    function createExchange(address token) external returns (address exchange);
    // Get Exchange and Token Info
    function getExchange(address token) external view returns (address exchange);
    function getToken(address exchange) external view returns (address token);
    function getTokenWithId(uint256 tokenId) external view returns (address token);
    // Initialize Factory
    function initializeFactory(address template) external;
}
```

## Exchange Interface

Coming soon...

## ERC20 Token Interface

Coming soon...




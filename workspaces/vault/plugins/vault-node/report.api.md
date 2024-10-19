## API Report File for "@backstage-community/plugin-vault-node"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { ExtensionPoint } from '@backstage/backend-plugin-api';

// @public
export interface VaultApi {
  getFrontendSecretsUrl(): string;
  listSecrets(
    secretPath: string,
    options?: {
      secretEngine?: string;
    },
  ): Promise<VaultSecret[]>;
  renewToken?(): Promise<void>;
}

// @public
export interface VaultExtensionPoint {
  // (undocumented)
  setClient(vaultClient: VaultApi): void;
}

// @public
export const vaultExtensionPoint: ExtensionPoint<VaultExtensionPoint>;

// @public
export type VaultSecret = {
  name: string;
  path: string;
  showUrl: string;
  editUrl: string;
};

// (No @packageDocumentation comment for this package)
```
---
title: Contact
sidebar_label: 'Contact'
---

# Contact Mixin

## Abstract Methods

### contactSelfName

```ts
abstract contactSelfName(name: string): Promise<void>
```

Set the name of bot self.

### contactSelfQRCode

```ts
abstract contactSelfQRCode(): Promise<string>
```

Get the qrcode of bot self.

### contactSelfSignature

```ts
abstract contactSelfSignature(signature: string): Promise<>
```

Set the signature of bot self.

### contactAlias

```ts
abstract contactAlias (contactId: string): Promise<string>
abstract contactAlias (contactId: string, alias: string | null) : Promise<void>
```

Set or get the alias of the contact.

### contactAvatar

```ts
abstract contactAvatar (contactId: string): Promise<FileBoxInterface>
abstract contactAvatar (contactId: string, file: FileBoxInterface): Promise<void>
```

Set or get the avatar of the contact.

### contactPhone

```ts
abstract contactPhone (contactId: string, phoneList: string[]) : Promise<void>

```

Set the phone list of the contact.

### contactCorporationRemark

```ts
abstract contactCorporationRemark (contactId: string, corporationRemark: string | null): Promise<void>
```

Set the corporation remark of the contact.

### contactDescription

```ts
abstract contactDescription (contactId: string, description: string | null): Promise<void>
```

Set the description of the contact.

### contactList

```ts
abstract contactList(): Promise<string[]>
```

Get the list of contact ids.

### contactPayload

```ts
abstract contactRawPayload (contactId: string): Promise<any>
abstract contactRawPayloadParser (rawPayload: any) : Promise<ContactPayload>
```

```contactRawPayload``` returns the raw payload of the contact generated by IM, and ```contactRawPayloadParser``` parse the raw payload and transfer it into wechaty payload.
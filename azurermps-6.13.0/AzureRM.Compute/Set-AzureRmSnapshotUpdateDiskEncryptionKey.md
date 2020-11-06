---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: 2a6f1fdc21b013e8a0aa0d34690b8e43319b306e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504466"
---
# <span data-ttu-id="c8d6d-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c8d6d-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="c8d6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d6d-103">Legt die Eigenschaften des Datenträger Verschlüsselungsschlüssels für ein Aktualisierungs Objekt für Snapshots fest.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8d6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8d6d-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8d6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8d6d-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d6d-106">Das Cmdlet " **Set-AzureRmSnapshotUpdateDiskEncryptionKey** " legt die Eigenschaften des Datenträger Verschlüsselungsschlüssels für ein Aktualisierungs Objekt für Snapshots fest.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-106">The **Set-AzureRmSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="c8d6d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8d6d-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d6d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c8d6d-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="c8d6d-109">Mit dem ersten Befehl wird ein lokales leeres Snapshot-Update Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="c8d6d-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c8d6d-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Update-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="c8d6d-112">Der letzte Befehl übernimmt das Aktualisierungs Objekt für Snapshots und aktualisiert einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c8d6d-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c8d6d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8d6d-113">PARAMETERS</span></span>

### <span data-ttu-id="c8d6d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d6d-114">-DefaultProfile</span></span>
<span data-ttu-id="c8d6d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d6d-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="c8d6d-116">-SecretUrl</span></span>
<span data-ttu-id="c8d6d-117">Gibt an der geheimen URL.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-117">Specifes the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d6d-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="c8d6d-118">-SnapshotUpdate</span></span>
<span data-ttu-id="c8d6d-119">Gibt ein lokales Aktualisierungs Objekt für Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d6d-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="c8d6d-120">-SourceVaultId</span></span>
<span data-ttu-id="c8d6d-121">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d6d-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8d6d-122">-Confirm</span></span>
<span data-ttu-id="c8d6d-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d6d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d6d-124">-WhatIf</span></span>
<span data-ttu-id="c8d6d-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8d6d-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d6d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d6d-127">CommonParameters</span></span>
<span data-ttu-id="c8d6d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d6d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d6d-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d6d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d6d-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8d6d-130">INPUTS</span></span>

### <span data-ttu-id="c8d6d-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="c8d6d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="c8d6d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c8d6d-132">System.String</span></span>

## <span data-ttu-id="c8d6d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8d6d-133">OUTPUTS</span></span>

### <span data-ttu-id="c8d6d-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="c8d6d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="c8d6d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8d6d-135">NOTES</span></span>

## <span data-ttu-id="c8d6d-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8d6d-136">RELATED LINKS</span></span>

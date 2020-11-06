---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
ms.openlocfilehash: 05e48bc312dcbbf317906fadb63b9777765032ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481314"
---
# <span data-ttu-id="a35ec-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a35ec-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="a35ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a35ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a35ec-103">Legt die Eigenschaften des Datenträger Verschlüsselungsschlüssels für ein Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="a35ec-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a35ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a35ec-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <Snapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a35ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a35ec-105">DESCRIPTION</span></span>
<span data-ttu-id="a35ec-106">Das Cmdlet " **Set-AzureRmSnapshotDiskEncryptionKey** " legt die Eigenschaften des Datenträger Verschlüsselungsschlüssels für ein Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="a35ec-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="a35ec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a35ec-107">EXAMPLES</span></span>

### <span data-ttu-id="a35ec-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a35ec-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="a35ec-109">Der erste Befehl erstellt ein lokales leeres snapshotobjekt mit der Größe 5GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="a35ec-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="a35ec-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a35ec-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a35ec-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="a35ec-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="a35ec-112">Der letzte Befehl übernimmt das Snapshot-Objekt und erstellt einen Schnappschuss mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a35ec-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a35ec-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a35ec-113">PARAMETERS</span></span>

### <span data-ttu-id="a35ec-114">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="a35ec-114">-SecretUrl</span></span>
<span data-ttu-id="a35ec-115">Gibt die geheime URL an.</span><span class="sxs-lookup"><span data-stu-id="a35ec-115">Specifies the secret Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a35ec-116">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="a35ec-116">-Snapshot</span></span>
<span data-ttu-id="a35ec-117">Gibt ein lokales Snapshot-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a35ec-117">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a35ec-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a35ec-118">-SourceVaultId</span></span>
<span data-ttu-id="a35ec-119">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="a35ec-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a35ec-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a35ec-120">-Confirm</span></span>
<span data-ttu-id="a35ec-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a35ec-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35ec-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a35ec-122">-WhatIf</span></span>
<span data-ttu-id="a35ec-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a35ec-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a35ec-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a35ec-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a35ec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35ec-125">CommonParameters</span></span>
<span data-ttu-id="a35ec-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a35ec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35ec-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a35ec-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35ec-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a35ec-128">INPUTS</span></span>

### <span data-ttu-id="a35ec-129">Microsoft. Azure. Management. Compute. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="a35ec-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="a35ec-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a35ec-130">System.String</span></span>

## <span data-ttu-id="a35ec-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a35ec-131">OUTPUTS</span></span>

### <span data-ttu-id="a35ec-132">Microsoft. Azure. Management. Compute. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="a35ec-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="a35ec-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a35ec-133">NOTES</span></span>

## <span data-ttu-id="a35ec-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a35ec-134">RELATED LINKS</span></span>


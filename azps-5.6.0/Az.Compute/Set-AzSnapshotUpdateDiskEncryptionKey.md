---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: 076968159b433e33c5e22581cd5de35173be27b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946216"
---
# <span data-ttu-id="966a5-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="966a5-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="966a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="966a5-102">SYNOPSIS</span></span>
<span data-ttu-id="966a5-103">Legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Snapshotupdateobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="966a5-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="966a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="966a5-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="966a5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="966a5-105">DESCRIPTION</span></span>
<span data-ttu-id="966a5-106">Das **Cmdlet Set-AzSnapshotUpdateDiskEncryptionKey** legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Snapshotupdateobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="966a5-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="966a5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="966a5-107">EXAMPLES</span></span>

### <span data-ttu-id="966a5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="966a5-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="966a5-109">Mit dem ersten Befehl wird ein lokales leeres Snapshotupdateobjekt mit der Größe 10 GB in Premium_LRS Speicherkontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="966a5-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="966a5-110">Außerdem wird der Windows -Betriebssystemtyp festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="966a5-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="966a5-111">Mit dem zweiten und dritten Befehl werden die Einstellungen für den Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüssel für das Snapshotupdateobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="966a5-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="966a5-112">Der letzte Befehl übernimmt das Snapshotupdateobjekt und aktualisiert eine vorhandene Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="966a5-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="966a5-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="966a5-113">PARAMETERS</span></span>

### <span data-ttu-id="966a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966a5-114">-DefaultProfile</span></span>
<span data-ttu-id="966a5-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="966a5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="966a5-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="966a5-116">-SecretUrl</span></span>
<span data-ttu-id="966a5-117">Gibt die geheime URL an.</span><span class="sxs-lookup"><span data-stu-id="966a5-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="966a5-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="966a5-118">-SnapshotUpdate</span></span>
<span data-ttu-id="966a5-119">Gibt ein lokales Snapshotupdateobjekt an.</span><span class="sxs-lookup"><span data-stu-id="966a5-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="966a5-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="966a5-120">-SourceVaultId</span></span>
<span data-ttu-id="966a5-121">Gibt die Quelltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="966a5-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="966a5-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="966a5-122">-Confirm</span></span>
<span data-ttu-id="966a5-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="966a5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="966a5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="966a5-124">-WhatIf</span></span>
<span data-ttu-id="966a5-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="966a5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="966a5-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="966a5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="966a5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966a5-127">CommonParameters</span></span>
<span data-ttu-id="966a5-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="966a5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966a5-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="966a5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966a5-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="966a5-130">INPUTS</span></span>

### <span data-ttu-id="966a5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="966a5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="966a5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="966a5-132">System.String</span></span>

## <span data-ttu-id="966a5-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="966a5-133">OUTPUTS</span></span>

### <span data-ttu-id="966a5-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="966a5-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="966a5-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="966a5-135">NOTES</span></span>

## <span data-ttu-id="966a5-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="966a5-136">RELATED LINKS</span></span>

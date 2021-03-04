---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c03056d9e563d9c96df54e1d3e37d4c9f86dc572
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946217"
---
# <span data-ttu-id="faf0b-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="faf0b-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="faf0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf0b-102">SYNOPSIS</span></span>
<span data-ttu-id="faf0b-103">Legt die Schlüsselverschlüsselungsschlüsseleigenschaften für ein Snapshotobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="faf0b-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="faf0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="faf0b-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faf0b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="faf0b-105">DESCRIPTION</span></span>
<span data-ttu-id="faf0b-106">Das **Cmdlet Set-AzSnapshotKeyEncryptionKey** legt die Schlüsselverschlüsselungsschlüsseleigenschaften für ein Snapshotobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="faf0b-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="faf0b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="faf0b-107">EXAMPLES</span></span>

### <span data-ttu-id="faf0b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="faf0b-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="faf0b-109">Mit dem ersten Befehl wird ein lokales leeres Snapshotobjekt mit der Größe 5 GB in Standard_LRS Speicherkontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="faf0b-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="faf0b-110">Außerdem wird der Windows -Betriebssystemtyp festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="faf0b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="faf0b-111">Mit dem zweiten und dritten Befehl werden die Einstellungen für den Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüssel für das Snapshotobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="faf0b-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="faf0b-112">Der letzte Befehl übernimmt das Snapshotobjekt und erstellt eine Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="faf0b-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="faf0b-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="faf0b-113">PARAMETERS</span></span>

### <span data-ttu-id="faf0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf0b-114">-DefaultProfile</span></span>
<span data-ttu-id="faf0b-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="faf0b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faf0b-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="faf0b-116">-KeyUrl</span></span>
<span data-ttu-id="faf0b-117">Gibt die Schlüssel-URL an.</span><span class="sxs-lookup"><span data-stu-id="faf0b-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="faf0b-118">-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="faf0b-118">-Snapshot</span></span>
<span data-ttu-id="faf0b-119">Gibt ein lokales Snapshotobjekt an.</span><span class="sxs-lookup"><span data-stu-id="faf0b-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faf0b-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="faf0b-120">-SourceVaultId</span></span>
<span data-ttu-id="faf0b-121">Gibt die Quelltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="faf0b-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="faf0b-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="faf0b-122">-Confirm</span></span>
<span data-ttu-id="faf0b-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="faf0b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faf0b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf0b-124">-WhatIf</span></span>
<span data-ttu-id="faf0b-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="faf0b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="faf0b-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="faf0b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faf0b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf0b-127">CommonParameters</span></span>
<span data-ttu-id="faf0b-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf0b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf0b-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faf0b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf0b-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="faf0b-130">INPUTS</span></span>

### <span data-ttu-id="faf0b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="faf0b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="faf0b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="faf0b-132">System.String</span></span>

## <span data-ttu-id="faf0b-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="faf0b-133">OUTPUTS</span></span>

### <span data-ttu-id="faf0b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="faf0b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="faf0b-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="faf0b-135">NOTES</span></span>

## <span data-ttu-id="faf0b-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="faf0b-136">RELATED LINKS</span></span>

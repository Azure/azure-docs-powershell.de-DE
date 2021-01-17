---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
ms.openlocfilehash: e4ecb281382af308176f47462e086f69c18e6163
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470849"
---
# <span data-ttu-id="f79ff-101">Set-AzSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f79ff-101">Set-AzSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="f79ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f79ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f79ff-103">Legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Momentaufnahmeobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="f79ff-103">Sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="f79ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f79ff-104">SYNTAX</span></span>

```
Set-AzSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f79ff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f79ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f79ff-106">Das **Cmdlet Set-AzSnapshotDiskEncryptionKey** legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Momentaufnahmeobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="f79ff-106">The **Set-AzSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="f79ff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f79ff-107">EXAMPLES</span></span>

### <span data-ttu-id="f79ff-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f79ff-108">Example 1</span></span>
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

<span data-ttu-id="f79ff-109">Der erste Befehl erstellt ein lokales leeres Momentaufnahmeobjekt mit einer Größe von 5 GB Standard_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="f79ff-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="f79ff-110">Außerdem wird der Typ des Windows-Betriebssystems festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f79ff-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="f79ff-111">Mit dem zweiten und dritten Befehl werden der Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüsseleinstellungen für das Momentaufnahmeobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f79ff-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="f79ff-112">Der letzte Befehl erstellt das Momentaufnahmeobjekt und erstellt eine Momentaufnahme mit dem Namen 'Snapshot01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="f79ff-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f79ff-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f79ff-113">PARAMETERS</span></span>

### <span data-ttu-id="f79ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79ff-114">-DefaultProfile</span></span>
<span data-ttu-id="f79ff-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f79ff-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f79ff-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="f79ff-116">-SecretUrl</span></span>
<span data-ttu-id="f79ff-117">Gibt die geheime URL an.</span><span class="sxs-lookup"><span data-stu-id="f79ff-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="f79ff-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="f79ff-118">-Snapshot</span></span>
<span data-ttu-id="f79ff-119">Gibt ein lokales Momentaufnahmeobjekt an.</span><span class="sxs-lookup"><span data-stu-id="f79ff-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="f79ff-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="f79ff-120">-SourceVaultId</span></span>
<span data-ttu-id="f79ff-121">Gibt die Quelltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="f79ff-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="f79ff-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f79ff-122">-Confirm</span></span>
<span data-ttu-id="f79ff-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f79ff-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f79ff-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f79ff-124">-WhatIf</span></span>
<span data-ttu-id="f79ff-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f79ff-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f79ff-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f79ff-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f79ff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79ff-127">CommonParameters</span></span>
<span data-ttu-id="f79ff-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f79ff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79ff-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f79ff-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79ff-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f79ff-130">INPUTS</span></span>

### <span data-ttu-id="f79ff-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="f79ff-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="f79ff-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f79ff-132">System.String</span></span>

## <span data-ttu-id="f79ff-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f79ff-133">OUTPUTS</span></span>

### <span data-ttu-id="f79ff-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="f79ff-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="f79ff-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f79ff-135">NOTES</span></span>

## <span data-ttu-id="f79ff-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f79ff-136">RELATED LINKS</span></span>

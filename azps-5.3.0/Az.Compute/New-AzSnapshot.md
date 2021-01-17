---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
ms.openlocfilehash: f22a5b4bc9b30e152827f1914bd03a4a6cee4971
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458192"
---
# <span data-ttu-id="43c3b-101">New-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="43c3b-101">New-AzSnapshot</span></span>

## <span data-ttu-id="43c3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="43c3b-103">Erstellt eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="43c3b-103">Creates a snapshot.</span></span>

## <span data-ttu-id="43c3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43c3b-104">SYNTAX</span></span>

```
New-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43c3b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="43c3b-106">Das **Cmdlet "New-AzSnapshot"** erstellt eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="43c3b-106">The **New-AzSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="43c3b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43c3b-107">EXAMPLES</span></span>

### <span data-ttu-id="43c3b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43c3b-108">Example 1</span></span>
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

<span data-ttu-id="43c3b-109">Der erste Befehl erstellt ein lokales leeres Momentaufnahmeobjekt mit einer Größe von 5 GB Standard_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="43c3b-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="43c3b-110">Außerdem wird der Typ des Windows-Betriebssystems festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="43c3b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="43c3b-111">Mit dem zweiten und dritten Befehl werden der Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüsseleinstellungen für das Momentaufnahmeobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="43c3b-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="43c3b-112">Der letzte Befehl erstellt das Momentaufnahmeobjekt und erstellt eine Momentaufnahme mit dem Namen 'Snapshot01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="43c3b-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="43c3b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43c3b-113">PARAMETERS</span></span>

### <span data-ttu-id="43c3b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43c3b-114">-AsJob</span></span>
<span data-ttu-id="43c3b-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="43c3b-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43c3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43c3b-116">-DefaultProfile</span></span>
<span data-ttu-id="43c3b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43c3b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43c3b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43c3b-118">-ResourceGroupName</span></span>
<span data-ttu-id="43c3b-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="43c3b-119">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c3b-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="43c3b-120">-Snapshot</span></span>
<span data-ttu-id="43c3b-121">Gibt ein lokales Momentaufnahmeobjekt an.</span><span class="sxs-lookup"><span data-stu-id="43c3b-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43c3b-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="43c3b-122">-SnapshotName</span></span>
<span data-ttu-id="43c3b-123">Gibt den Namen einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="43c3b-123">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43c3b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43c3b-124">-Confirm</span></span>
<span data-ttu-id="43c3b-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43c3b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43c3b-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="43c3b-126">-WhatIf</span></span>
<span data-ttu-id="43c3b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43c3b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43c3b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43c3b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43c3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43c3b-129">CommonParameters</span></span>
<span data-ttu-id="43c3b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43c3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43c3b-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43c3b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43c3b-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43c3b-132">INPUTS</span></span>

### <span data-ttu-id="43c3b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="43c3b-133">System.String</span></span>

### <span data-ttu-id="43c3b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="43c3b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="43c3b-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43c3b-135">OUTPUTS</span></span>

### <span data-ttu-id="43c3b-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="43c3b-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="43c3b-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="43c3b-137">NOTES</span></span>

## <span data-ttu-id="43c3b-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="43c3b-138">RELATED LINKS</span></span>

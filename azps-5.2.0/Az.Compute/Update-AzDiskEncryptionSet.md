---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295517"
---
# <span data-ttu-id="43679-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="43679-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="43679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43679-102">SYNOPSIS</span></span>
<span data-ttu-id="43679-103">Aktualisiert einen Datenträgerverschlüsselungssatz.</span><span class="sxs-lookup"><span data-stu-id="43679-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="43679-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43679-104">SYNTAX</span></span>

### <span data-ttu-id="43679-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="43679-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43679-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="43679-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43679-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="43679-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43679-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43679-108">DESCRIPTION</span></span>
<span data-ttu-id="43679-109">Aktualisiert einen Datenträgerverschlüsselungssatz.</span><span class="sxs-lookup"><span data-stu-id="43679-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="43679-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43679-110">EXAMPLES</span></span>

### <span data-ttu-id="43679-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43679-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="43679-112">Aktualisiert den Datenträgerverschlüsselungssatz mit dem angegebenen aktiven Schlüssel im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="43679-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="43679-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43679-113">PARAMETERS</span></span>

### <span data-ttu-id="43679-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43679-114">-AsJob</span></span>
<span data-ttu-id="43679-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="43679-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43679-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43679-116">-DefaultProfile</span></span>
<span data-ttu-id="43679-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43679-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43679-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43679-118">-InputObject</span></span>
<span data-ttu-id="43679-119">Das lokale Objekt des Datenträgerverschlüsselungssets.</span><span class="sxs-lookup"><span data-stu-id="43679-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43679-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="43679-120">-KeyUrl</span></span>
<span data-ttu-id="43679-121">URL, die auf den aktiven Schlüssel in KeyVault verweist</span><span class="sxs-lookup"><span data-stu-id="43679-121">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43679-122">-Name</span><span class="sxs-lookup"><span data-stu-id="43679-122">-Name</span></span>
<span data-ttu-id="43679-123">Name des Datenträgerverschlüsselungssatzs.</span><span class="sxs-lookup"><span data-stu-id="43679-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43679-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43679-124">-ResourceGroupName</span></span>
<span data-ttu-id="43679-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="43679-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43679-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43679-126">-ResourceId</span></span>
<span data-ttu-id="43679-127">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="43679-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43679-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="43679-128">-SourceVaultId</span></span>
<span data-ttu-id="43679-129">Ressourcen-ID des KeyVault, der den aktiven Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="43679-129">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43679-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="43679-130">-Tag</span></span>
<span data-ttu-id="43679-131">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="43679-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="43679-132">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="43679-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43679-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43679-133">-Confirm</span></span>
<span data-ttu-id="43679-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43679-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43679-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="43679-135">-WhatIf</span></span>
<span data-ttu-id="43679-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43679-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43679-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43679-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43679-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43679-138">CommonParameters</span></span>
<span data-ttu-id="43679-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43679-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43679-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43679-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43679-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43679-141">INPUTS</span></span>

### <span data-ttu-id="43679-142">System.String</span><span class="sxs-lookup"><span data-stu-id="43679-142">System.String</span></span>

### <span data-ttu-id="43679-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="43679-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="43679-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="43679-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="43679-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43679-145">OUTPUTS</span></span>

### <span data-ttu-id="43679-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="43679-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="43679-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="43679-147">NOTES</span></span>

## <span data-ttu-id="43679-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="43679-148">RELATED LINKS</span></span>

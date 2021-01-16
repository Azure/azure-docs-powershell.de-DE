---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358712"
---
# <span data-ttu-id="45291-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="45291-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="45291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45291-102">SYNOPSIS</span></span>
<span data-ttu-id="45291-103">Entfernt die Anmeldeinformationen eines Speicherkontos für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="45291-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="45291-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45291-104">SYNTAX</span></span>

### <span data-ttu-id="45291-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="45291-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45291-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45291-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45291-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45291-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45291-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45291-108">DESCRIPTION</span></span>
<span data-ttu-id="45291-109">Das **Cmdlet "Remove-AzStackEdgeStorageAccountCredential"** entfernt die Anmeldeinformationen des Speicherkontos für ein Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="45291-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="45291-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45291-110">EXAMPLES</span></span>

### <span data-ttu-id="45291-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="45291-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="45291-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45291-112">PARAMETERS</span></span>

### <span data-ttu-id="45291-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45291-113">-AsJob</span></span>
<span data-ttu-id="45291-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="45291-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45291-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45291-115">-DefaultProfile</span></span>
<span data-ttu-id="45291-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45291-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45291-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="45291-117">-DeviceName</span></span>
<span data-ttu-id="45291-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="45291-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45291-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45291-119">-InputObject</span></span>
<span data-ttu-id="45291-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="45291-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45291-121">-Name</span><span class="sxs-lookup"><span data-stu-id="45291-121">-Name</span></span>
<span data-ttu-id="45291-122">Name des zu verwendende Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="45291-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45291-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45291-123">-PassThru</span></span>
<span data-ttu-id="45291-124">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="45291-124">returns true if successful</span></span>

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

### <span data-ttu-id="45291-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45291-125">-ResourceGroupName</span></span>
<span data-ttu-id="45291-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="45291-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45291-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45291-127">-ResourceId</span></span>
<span data-ttu-id="45291-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="45291-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45291-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45291-129">-Confirm</span></span>
<span data-ttu-id="45291-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45291-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45291-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="45291-131">-WhatIf</span></span>
<span data-ttu-id="45291-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45291-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45291-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45291-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45291-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45291-134">CommonParameters</span></span>
<span data-ttu-id="45291-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45291-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45291-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45291-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45291-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45291-137">INPUTS</span></span>

### <span data-ttu-id="45291-138">System.String</span><span class="sxs-lookup"><span data-stu-id="45291-138">System.String</span></span>

### <span data-ttu-id="45291-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="45291-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="45291-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45291-140">OUTPUTS</span></span>

### <span data-ttu-id="45291-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45291-141">System.Boolean</span></span>

## <span data-ttu-id="45291-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45291-142">NOTES</span></span>

## <span data-ttu-id="45291-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45291-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 74531aa3c5e142cf3c9638f4910c8d45654a20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936779"
---
# <span data-ttu-id="74d6c-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="74d6c-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="74d6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="74d6c-103">Ändert eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="74d6c-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="74d6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74d6c-104">SYNTAX</span></span>

### <span data-ttu-id="74d6c-105">ByIntegrationAccountAndFilePath (Standard)</span><span class="sxs-lookup"><span data-stu-id="74d6c-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d6c-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="74d6c-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74d6c-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="74d6c-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74d6c-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="74d6c-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d6c-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="74d6c-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d6c-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="74d6c-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d6c-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="74d6c-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d6c-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="74d6c-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74d6c-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="74d6c-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74d6c-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74d6c-114">DESCRIPTION</span></span>
<span data-ttu-id="74d6c-115">Das **Cmdlet Set-AzIntegrationAccountAssembly** ändert eine Integrationskontoassemblet.</span><span class="sxs-lookup"><span data-stu-id="74d6c-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="74d6c-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74d6c-116">EXAMPLES</span></span>

### <span data-ttu-id="74d6c-117">Beispiel 1: Ändern einer Assembly mithilfe der lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="74d6c-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="74d6c-118">Ändert die Assembly mit dem Namen "sampleAssembly" mithilfe der lokalen Datei, die sich im Dateipfad befindet, der in "$localAssemblyFilePath" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="74d6c-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="74d6c-119">Beispiel 2: Ändern einer Assembly mithilfe von Bytedaten</span><span class="sxs-lookup"><span data-stu-id="74d6c-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="74d6c-120">Ändert die Assembly mit dem Namen "sampleAssembly" mithilfe des in "$assemblyContent" enthaltenen Bytearrays.</span><span class="sxs-lookup"><span data-stu-id="74d6c-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="74d6c-121">Beispiel 3: Ändern einer Assembly mithilfe eines Inhaltslinks</span><span class="sxs-lookup"><span data-stu-id="74d6c-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="74d6c-122">Ändert die Assembly mit dem Namen "sampleAssembly" mithilfe der Bytedaten, die sich unter der URL "$assemblyUrl" befinden.</span><span class="sxs-lookup"><span data-stu-id="74d6c-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="74d6c-123">Dies ist die vorgeschlagene Methode zum Erstellen großer Assemblys.</span><span class="sxs-lookup"><span data-stu-id="74d6c-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="74d6c-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="74d6c-124">PARAMETERS</span></span>

### <span data-ttu-id="74d6c-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="74d6c-125">-AssemblyData</span></span>
<span data-ttu-id="74d6c-126">Die Bytedaten der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="74d6c-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d6c-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="74d6c-127">-AssemblyFilePath</span></span>
<span data-ttu-id="74d6c-128">Der Dateipfad der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="74d6c-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d6c-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="74d6c-129">-ContentLink</span></span>
<span data-ttu-id="74d6c-130">Ein öffentlich zugänglicher Link zu den Assemblydaten des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="74d6c-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d6c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d6c-131">-DefaultProfile</span></span>
<span data-ttu-id="74d6c-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74d6c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74d6c-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74d6c-133">-InputObject</span></span>
<span data-ttu-id="74d6c-134">Eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="74d6c-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74d6c-135">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="74d6c-135">-Metadata</span></span>
<span data-ttu-id="74d6c-136">Die Metadaten der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="74d6c-136">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d6c-137">-Name</span><span class="sxs-lookup"><span data-stu-id="74d6c-137">-Name</span></span>
<span data-ttu-id="74d6c-138">Der Assemblyname des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="74d6c-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d6c-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="74d6c-139">-ParentName</span></span>
<span data-ttu-id="74d6c-140">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="74d6c-140">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d6c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d6c-141">-ResourceGroupName</span></span>
<span data-ttu-id="74d6c-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74d6c-142">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74d6c-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74d6c-143">-ResourceId</span></span>
<span data-ttu-id="74d6c-144">Die Ressourcen-ID der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="74d6c-144">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74d6c-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74d6c-145">-Confirm</span></span>
<span data-ttu-id="74d6c-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74d6c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d6c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d6c-147">-WhatIf</span></span>
<span data-ttu-id="74d6c-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74d6c-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74d6c-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74d6c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d6c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d6c-150">CommonParameters</span></span>
<span data-ttu-id="74d6c-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d6c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d6c-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74d6c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d6c-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74d6c-153">INPUTS</span></span>

### <span data-ttu-id="74d6c-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="74d6c-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="74d6c-155">System.String</span><span class="sxs-lookup"><span data-stu-id="74d6c-155">System.String</span></span>

## <span data-ttu-id="74d6c-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74d6c-156">OUTPUTS</span></span>

### <span data-ttu-id="74d6c-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="74d6c-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="74d6c-158">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="74d6c-158">NOTES</span></span>

## <span data-ttu-id="74d6c-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="74d6c-159">RELATED LINKS</span></span>

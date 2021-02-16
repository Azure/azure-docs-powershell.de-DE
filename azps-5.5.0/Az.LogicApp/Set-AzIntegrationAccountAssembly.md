---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157548"
---
# <span data-ttu-id="99e70-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="99e70-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="99e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e70-102">SYNOPSIS</span></span>
<span data-ttu-id="99e70-103">Ändert eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="99e70-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="99e70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99e70-104">SYNTAX</span></span>

### <span data-ttu-id="99e70-105">ByIntegrationAccountAndFilePath (Standard)</span><span class="sxs-lookup"><span data-stu-id="99e70-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e70-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="99e70-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99e70-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="99e70-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99e70-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="99e70-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e70-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="99e70-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e70-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="99e70-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e70-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="99e70-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e70-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="99e70-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99e70-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="99e70-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99e70-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99e70-114">DESCRIPTION</span></span>
<span data-ttu-id="99e70-115">Das **Cmdlet "Set-AzIntegrationAccountAssembly"** ändert eine Integrationskontoassembly.</span><span class="sxs-lookup"><span data-stu-id="99e70-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="99e70-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99e70-116">EXAMPLES</span></span>

### <span data-ttu-id="99e70-117">Beispiel 1: Ändern einer Assembly mithilfe einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="99e70-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="99e70-118">Ändert die Assembly namens "sampleAssembly" mit der lokalen Datei, die sich im Dateipfad in "$localAssemblyFilePath" befindet.</span><span class="sxs-lookup"><span data-stu-id="99e70-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="99e70-119">Beispiel 2: Ändern einer Assembly mithilfe von Bytedaten</span><span class="sxs-lookup"><span data-stu-id="99e70-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="99e70-120">Ändert die Assembly mit dem Namen "sampleAssembly" und verwendet dabei ein Bytearray, das in "$assemblyContent" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="99e70-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="99e70-121">Beispiel 3: Ändern einer Assembly mithilfe eines Inhaltslinks</span><span class="sxs-lookup"><span data-stu-id="99e70-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="99e70-122">Ändert die Assembly mit dem Namen "sampleAssembly" und verwendet dabei die Bytedaten, die sich unter der URL "$assemblyUrl" befinden.</span><span class="sxs-lookup"><span data-stu-id="99e70-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="99e70-123">Dies ist die vorgeschlagene Methode zum Erstellen großer Assemblys.</span><span class="sxs-lookup"><span data-stu-id="99e70-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="99e70-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99e70-124">PARAMETERS</span></span>

### <span data-ttu-id="99e70-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="99e70-125">-AssemblyData</span></span>
<span data-ttu-id="99e70-126">Bytedaten für die Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="99e70-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="99e70-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="99e70-127">-AssemblyFilePath</span></span>
<span data-ttu-id="99e70-128">Der Dateipfad der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="99e70-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="99e70-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="99e70-129">-ContentLink</span></span>
<span data-ttu-id="99e70-130">Eine öffentlich zugängliche Verknüpfung zu den Assemblydaten des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="99e70-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="99e70-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e70-131">-DefaultProfile</span></span>
<span data-ttu-id="99e70-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99e70-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99e70-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99e70-133">-InputObject</span></span>
<span data-ttu-id="99e70-134">Eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="99e70-134">An integration account assembly.</span></span>

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

### <span data-ttu-id="99e70-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="99e70-135">-Metadata</span></span>
<span data-ttu-id="99e70-136">Die Metadaten der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="99e70-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="99e70-137">-Name</span><span class="sxs-lookup"><span data-stu-id="99e70-137">-Name</span></span>
<span data-ttu-id="99e70-138">Der Name der Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="99e70-138">The integration account assembly name.</span></span>

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

### <span data-ttu-id="99e70-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="99e70-139">-ParentName</span></span>
<span data-ttu-id="99e70-140">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="99e70-140">The integration account name.</span></span>

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

### <span data-ttu-id="99e70-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e70-141">-ResourceGroupName</span></span>
<span data-ttu-id="99e70-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99e70-142">The resource group name.</span></span>

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

### <span data-ttu-id="99e70-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99e70-143">-ResourceId</span></span>
<span data-ttu-id="99e70-144">Die Ressourcen-ID der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="99e70-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="99e70-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99e70-145">-Confirm</span></span>
<span data-ttu-id="99e70-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99e70-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99e70-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="99e70-147">-WhatIf</span></span>
<span data-ttu-id="99e70-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99e70-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99e70-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99e70-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99e70-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e70-150">CommonParameters</span></span>
<span data-ttu-id="99e70-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e70-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e70-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e70-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e70-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99e70-153">INPUTS</span></span>

### <span data-ttu-id="99e70-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="99e70-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="99e70-155">System.String</span><span class="sxs-lookup"><span data-stu-id="99e70-155">System.String</span></span>

## <span data-ttu-id="99e70-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99e70-156">OUTPUTS</span></span>

### <span data-ttu-id="99e70-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="99e70-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="99e70-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="99e70-158">NOTES</span></span>

## <span data-ttu-id="99e70-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="99e70-159">RELATED LINKS</span></span>

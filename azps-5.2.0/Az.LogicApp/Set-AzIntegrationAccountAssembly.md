---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300344"
---
# <span data-ttu-id="59f10-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59f10-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="59f10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f10-102">SYNOPSIS</span></span>
<span data-ttu-id="59f10-103">Ändert eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="59f10-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="59f10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59f10-104">SYNTAX</span></span>

### <span data-ttu-id="59f10-105">ByIntegrationAccountAndFilePath (Standard)</span><span class="sxs-lookup"><span data-stu-id="59f10-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f10-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="59f10-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59f10-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="59f10-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59f10-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="59f10-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f10-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="59f10-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f10-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="59f10-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f10-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="59f10-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f10-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="59f10-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f10-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="59f10-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59f10-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59f10-114">DESCRIPTION</span></span>
<span data-ttu-id="59f10-115">Das **Cmdlet "Set-AzIntegrationAccountAssembly"** ändert eine Integrationskontoassembly.</span><span class="sxs-lookup"><span data-stu-id="59f10-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="59f10-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59f10-116">EXAMPLES</span></span>

### <span data-ttu-id="59f10-117">Beispiel 1: Ändern einer Assembly mithilfe einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="59f10-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="59f10-118">Ändert die Assembly namens "sampleAssembly" mit der lokalen Datei, die sich im Dateipfad in "$localAssemblyFilePath" befindet.</span><span class="sxs-lookup"><span data-stu-id="59f10-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="59f10-119">Beispiel 2: Ändern einer Assembly mithilfe von Bytedaten</span><span class="sxs-lookup"><span data-stu-id="59f10-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="59f10-120">Ändert die Assembly namens "sampleAssembly" mit dem byte-Array, das in "$assemblyContent" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="59f10-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="59f10-121">Beispiel 3: Ändern einer Assembly mithilfe eines Inhaltslinks</span><span class="sxs-lookup"><span data-stu-id="59f10-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="59f10-122">Ändert die Assembly mit dem Namen "sampleAssembly" und verwendet dabei die Bytedaten, die sich unter der URL "$assemblyUrl" befinden.</span><span class="sxs-lookup"><span data-stu-id="59f10-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="59f10-123">Dies ist die vorgeschlagene Methode zum Erstellen großer Assemblys.</span><span class="sxs-lookup"><span data-stu-id="59f10-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="59f10-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59f10-124">PARAMETERS</span></span>

### <span data-ttu-id="59f10-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="59f10-125">-AssemblyData</span></span>
<span data-ttu-id="59f10-126">Bytedaten für die Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="59f10-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="59f10-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="59f10-127">-AssemblyFilePath</span></span>
<span data-ttu-id="59f10-128">Der Dateipfad der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="59f10-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="59f10-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="59f10-129">-ContentLink</span></span>
<span data-ttu-id="59f10-130">Eine öffentlich zugängliche Verknüpfung zu den Assemblydaten des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="59f10-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="59f10-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f10-131">-DefaultProfile</span></span>
<span data-ttu-id="59f10-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59f10-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59f10-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59f10-133">-InputObject</span></span>
<span data-ttu-id="59f10-134">Eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="59f10-134">An integration account assembly.</span></span>

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

### <span data-ttu-id="59f10-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="59f10-135">-Metadata</span></span>
<span data-ttu-id="59f10-136">Die Metadaten der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="59f10-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="59f10-137">-Name</span><span class="sxs-lookup"><span data-stu-id="59f10-137">-Name</span></span>
<span data-ttu-id="59f10-138">Der Name der Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="59f10-138">The integration account assembly name.</span></span>

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

### <span data-ttu-id="59f10-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="59f10-139">-ParentName</span></span>
<span data-ttu-id="59f10-140">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="59f10-140">The integration account name.</span></span>

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

### <span data-ttu-id="59f10-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f10-141">-ResourceGroupName</span></span>
<span data-ttu-id="59f10-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59f10-142">The resource group name.</span></span>

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

### <span data-ttu-id="59f10-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59f10-143">-ResourceId</span></span>
<span data-ttu-id="59f10-144">Die Ressourcen-ID der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="59f10-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="59f10-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59f10-145">-Confirm</span></span>
<span data-ttu-id="59f10-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59f10-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59f10-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="59f10-147">-WhatIf</span></span>
<span data-ttu-id="59f10-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59f10-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59f10-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59f10-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59f10-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f10-150">CommonParameters</span></span>
<span data-ttu-id="59f10-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59f10-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f10-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f10-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f10-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59f10-153">INPUTS</span></span>

### <span data-ttu-id="59f10-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59f10-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="59f10-155">System.String</span><span class="sxs-lookup"><span data-stu-id="59f10-155">System.String</span></span>

## <span data-ttu-id="59f10-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59f10-156">OUTPUTS</span></span>

### <span data-ttu-id="59f10-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="59f10-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="59f10-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59f10-158">NOTES</span></span>

## <span data-ttu-id="59f10-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59f10-159">RELATED LINKS</span></span>

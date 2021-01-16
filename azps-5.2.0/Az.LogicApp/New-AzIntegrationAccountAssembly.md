---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290224"
---
# <span data-ttu-id="4338e-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4338e-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="4338e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4338e-102">SYNOPSIS</span></span>
<span data-ttu-id="4338e-103">Erstellt eine Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="4338e-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="4338e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4338e-104">SYNTAX</span></span>

### <span data-ttu-id="4338e-105">ByIntegrationAccountAndFilePath (Standard)</span><span class="sxs-lookup"><span data-stu-id="4338e-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4338e-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="4338e-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4338e-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="4338e-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4338e-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="4338e-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4338e-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="4338e-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4338e-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="4338e-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4338e-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="4338e-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4338e-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="4338e-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4338e-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="4338e-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4338e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4338e-114">DESCRIPTION</span></span>
<span data-ttu-id="4338e-115">Das **Cmdlet "Get-AzIntegrationAccountAssembly"** erstellt eine neue Assembly in einem Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="4338e-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="4338e-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4338e-116">EXAMPLES</span></span>

### <span data-ttu-id="4338e-117">Beispiel 1: Erstellen einer neuen Assembly mithilfe einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="4338e-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="4338e-118">Erstellt eine neue Assembly unter Verwendung der lokalen Datei, die sich im Dateipfad in "$localAssemblyFilePath" befindet.</span><span class="sxs-lookup"><span data-stu-id="4338e-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="4338e-119">Beispiel 2: Erstellen einer neuen Assembly mithilfe von Bytedaten</span><span class="sxs-lookup"><span data-stu-id="4338e-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="4338e-120">Erstellt eine neue Assembly mit dem byte-Array, das in "$assemblyContent" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4338e-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="4338e-121">Beispiel 3: Erstellen einer neuen Assembly mithilfe eines Inhaltslinks</span><span class="sxs-lookup"><span data-stu-id="4338e-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="4338e-122">Erstellt eine neue Assembly mithilfe der Bytedaten, die sich unter der URL "$assemblyUrl" befinden.</span><span class="sxs-lookup"><span data-stu-id="4338e-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="4338e-123">Dies ist die vorgeschlagene Methode zum Erstellen großer Assemblys.</span><span class="sxs-lookup"><span data-stu-id="4338e-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="4338e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4338e-124">PARAMETERS</span></span>

### <span data-ttu-id="4338e-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="4338e-125">-AssemblyData</span></span>
<span data-ttu-id="4338e-126">Bytedaten für die Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="4338e-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="4338e-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="4338e-127">-AssemblyFilePath</span></span>
<span data-ttu-id="4338e-128">Der Dateipfad der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="4338e-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="4338e-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="4338e-129">-ContentLink</span></span>
<span data-ttu-id="4338e-130">Eine öffentlich zugängliche Verknüpfung zu den Assemblydaten des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="4338e-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="4338e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4338e-131">-DefaultProfile</span></span>
<span data-ttu-id="4338e-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4338e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4338e-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4338e-133">-Metadata</span></span>
<span data-ttu-id="4338e-134">Die Metadaten der Integrationskonto-Assembly.</span><span class="sxs-lookup"><span data-stu-id="4338e-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="4338e-135">-Name</span><span class="sxs-lookup"><span data-stu-id="4338e-135">-Name</span></span>
<span data-ttu-id="4338e-136">Der Name der Integrationskonto assembly.</span><span class="sxs-lookup"><span data-stu-id="4338e-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4338e-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="4338e-137">-ParentName</span></span>
<span data-ttu-id="4338e-138">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="4338e-138">The integration account name.</span></span>

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

### <span data-ttu-id="4338e-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4338e-139">-ParentObject</span></span>
<span data-ttu-id="4338e-140">Ein Integrationskontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="4338e-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4338e-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4338e-141">-ParentResourceId</span></span>
<span data-ttu-id="4338e-142">Die Ressourcen-ID des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="4338e-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="4338e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4338e-143">-ResourceGroupName</span></span>
<span data-ttu-id="4338e-144">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4338e-144">The resource group name.</span></span>

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

### <span data-ttu-id="4338e-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4338e-145">-Confirm</span></span>
<span data-ttu-id="4338e-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4338e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4338e-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4338e-147">-WhatIf</span></span>
<span data-ttu-id="4338e-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4338e-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4338e-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4338e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4338e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4338e-150">CommonParameters</span></span>
<span data-ttu-id="4338e-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4338e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4338e-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4338e-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4338e-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4338e-153">INPUTS</span></span>

### <span data-ttu-id="4338e-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4338e-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="4338e-155">System.String</span><span class="sxs-lookup"><span data-stu-id="4338e-155">System.String</span></span>

## <span data-ttu-id="4338e-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4338e-156">OUTPUTS</span></span>

### <span data-ttu-id="4338e-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4338e-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="4338e-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4338e-158">NOTES</span></span>

## <span data-ttu-id="4338e-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4338e-159">RELATED LINKS</span></span>

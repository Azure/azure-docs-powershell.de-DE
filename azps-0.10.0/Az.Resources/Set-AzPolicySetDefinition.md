---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 21ea2a78ed14cc7fbcc343bd7905a33ef4bd126a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843196"
---
# <span data-ttu-id="f95a8-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f95a8-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="f95a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f95a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f95a8-103">Ändert eine Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="f95a8-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="f95a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f95a8-104">SYNTAX</span></span>

### <span data-ttu-id="f95a8-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f95a8-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f95a8-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95a8-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f95a8-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95a8-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f95a8-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95a8-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f95a8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f95a8-109">DESCRIPTION</span></span>
<span data-ttu-id="f95a8-110">Das Cmdlet " **Satz-AzPolicySetDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="f95a8-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="f95a8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f95a8-111">EXAMPLES</span></span>

### <span data-ttu-id="f95a8-112">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="f95a8-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="f95a8-113">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="f95a8-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="f95a8-114">Der Befehl speichert das Objekt in der $PolicySetDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="f95a8-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="f95a8-115">Mit dem zweiten Befehl wird die Beschreibung der Richtliniensatz Definition aktualisiert, die durch die Eigenschaft " **Resourcen** " von $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="f95a8-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="f95a8-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f95a8-116">PARAMETERS</span></span>

### <span data-ttu-id="f95a8-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f95a8-117">-ApiVersion</span></span>
<span data-ttu-id="f95a8-118">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f95a8-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f95a8-119">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f95a8-119">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95a8-120">-DefaultProfile</span></span>
<span data-ttu-id="f95a8-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f95a8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95a8-122">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f95a8-122">-Description</span></span>
<span data-ttu-id="f95a8-123">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="f95a8-123">The description for policy set definition.</span></span>

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

### <span data-ttu-id="f95a8-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f95a8-124">-DisplayName</span></span>
<span data-ttu-id="f95a8-125">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="f95a8-125">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="f95a8-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f95a8-126">-Id</span></span>
<span data-ttu-id="f95a8-127">Die vollqualifizierte Richtlinien Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="f95a8-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="f95a8-128">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f95a8-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95a8-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f95a8-129">-ManagementGroupName</span></span>
<span data-ttu-id="f95a8-130">Der Name der Verwaltungsgruppe der Richtliniensatz Definition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f95a8-130">The name of the management group of the policy set definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95a8-131">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="f95a8-131">-Metadata</span></span>
<span data-ttu-id="f95a8-132">Die Metadaten der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="f95a8-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="f95a8-133">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f95a8-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="f95a8-134">-Name</span><span class="sxs-lookup"><span data-stu-id="f95a8-134">-Name</span></span>
<span data-ttu-id="f95a8-135">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="f95a8-135">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95a8-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f95a8-136">-Parameter</span></span>
<span data-ttu-id="f95a8-137">Die Parameters-Deklaration der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="f95a8-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="f95a8-138">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f95a8-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="f95a8-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f95a8-139">-PolicyDefinition</span></span>
<span data-ttu-id="f95a8-140">Die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="f95a8-140">The policy set definition.</span></span> <span data-ttu-id="f95a8-141">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtliniensatz Definition als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f95a8-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="f95a8-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="f95a8-142">-Pre</span></span>
<span data-ttu-id="f95a8-143">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="f95a8-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f95a8-144">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f95a8-144">-SubscriptionId</span></span>
<span data-ttu-id="f95a8-145">Die Abonnement-ID der Richtliniensatz Definition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f95a8-145">The subscription ID of the policy set definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95a8-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f95a8-146">-Confirm</span></span>
<span data-ttu-id="f95a8-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f95a8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95a8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f95a8-148">-WhatIf</span></span>
<span data-ttu-id="f95a8-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f95a8-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f95a8-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f95a8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95a8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95a8-151">CommonParameters</span></span>
<span data-ttu-id="f95a8-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95a8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95a8-153">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f95a8-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95a8-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f95a8-154">INPUTS</span></span>

### <span data-ttu-id="f95a8-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f95a8-155">System.String</span></span>

### <span data-ttu-id="f95a8-156">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f95a8-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f95a8-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f95a8-157">OUTPUTS</span></span>

### <span data-ttu-id="f95a8-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f95a8-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f95a8-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="f95a8-159">NOTES</span></span>

## <span data-ttu-id="f95a8-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f95a8-160">RELATED LINKS</span></span>

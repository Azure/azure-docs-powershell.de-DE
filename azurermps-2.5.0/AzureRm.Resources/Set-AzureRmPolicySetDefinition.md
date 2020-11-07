---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
ms.openlocfilehash: 2e5bc38e8fa98160df66cdfc29bbd249ab56b809
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850528"
---
# <span data-ttu-id="8f44f-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="8f44f-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="8f44f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f44f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f44f-103">Ändert eine Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="8f44f-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f44f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f44f-104">SYNTAX</span></span>

### <span data-ttu-id="8f44f-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f44f-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f44f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f44f-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f44f-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f44f-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f44f-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f44f-108">IdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f44f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f44f-109">DESCRIPTION</span></span>
<span data-ttu-id="8f44f-110">Das Cmdlet " **Satz-AzureRmPolicySetDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="8f44f-110">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="8f44f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f44f-111">EXAMPLES</span></span>

### <span data-ttu-id="8f44f-112">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="8f44f-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="8f44f-113">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzureRmPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="8f44f-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="8f44f-114">Der Befehl speichert das Objekt in der $PolicySetDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="8f44f-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="8f44f-115">Mit dem zweiten Befehl wird die Beschreibung der Richtliniensatz Definition aktualisiert, die durch die Eigenschaft " **Resourcen** " von $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="8f44f-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="8f44f-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f44f-116">PARAMETERS</span></span>

### <span data-ttu-id="8f44f-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8f44f-117">-ApiVersion</span></span>
<span data-ttu-id="8f44f-118">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f44f-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8f44f-119">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8f44f-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8f44f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f44f-120">-DefaultProfile</span></span>
<span data-ttu-id="8f44f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8f44f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f44f-122">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f44f-122">-Description</span></span>
<span data-ttu-id="8f44f-123">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="8f44f-123">The description for policy set definition.</span></span>

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

### <span data-ttu-id="8f44f-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8f44f-124">-DisplayName</span></span>
<span data-ttu-id="8f44f-125">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="8f44f-125">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="8f44f-126">-ID</span><span class="sxs-lookup"><span data-stu-id="8f44f-126">-Id</span></span>
<span data-ttu-id="8f44f-127">Die vollqualifizierte Richtlinien Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="8f44f-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="8f44f-128">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="8f44f-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="8f44f-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8f44f-129">-ManagementGroupName</span></span>
<span data-ttu-id="8f44f-130">Der Name der Verwaltungsgruppe der Richtliniensatz Definition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f44f-130">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="8f44f-131">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="8f44f-131">-Metadata</span></span>
<span data-ttu-id="8f44f-132">Die Metadaten der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="8f44f-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="8f44f-133">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8f44f-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="8f44f-134">-Name</span><span class="sxs-lookup"><span data-stu-id="8f44f-134">-Name</span></span>
<span data-ttu-id="8f44f-135">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="8f44f-135">The policy set definition name.</span></span>

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

### <span data-ttu-id="8f44f-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8f44f-136">-Parameter</span></span>
<span data-ttu-id="8f44f-137">Die Parameters-Deklaration der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="8f44f-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="8f44f-138">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8f44f-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="8f44f-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8f44f-139">-PolicyDefinition</span></span>
<span data-ttu-id="8f44f-140">Die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="8f44f-140">The policy set definition.</span></span> <span data-ttu-id="8f44f-141">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtliniensatz Definition als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8f44f-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="8f44f-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="8f44f-142">-Pre</span></span>
<span data-ttu-id="8f44f-143">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="8f44f-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8f44f-144">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8f44f-144">-SubscriptionId</span></span>
<span data-ttu-id="8f44f-145">Die Abonnement-ID der Richtliniensatz Definition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f44f-145">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="8f44f-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f44f-146">-Confirm</span></span>
<span data-ttu-id="8f44f-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f44f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f44f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f44f-148">-WhatIf</span></span>
<span data-ttu-id="8f44f-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f44f-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f44f-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f44f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f44f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f44f-151">CommonParameters</span></span>
<span data-ttu-id="8f44f-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f44f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f44f-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f44f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f44f-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f44f-154">INPUTS</span></span>

### <span data-ttu-id="8f44f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="8f44f-155">System.String</span></span>

### <span data-ttu-id="8f44f-156">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8f44f-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8f44f-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f44f-157">OUTPUTS</span></span>

### <span data-ttu-id="8f44f-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8f44f-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8f44f-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f44f-159">NOTES</span></span>

## <span data-ttu-id="8f44f-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f44f-160">RELATED LINKS</span></span>

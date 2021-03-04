---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 14da2ddfdd94be5cd95d00eeeb742b9e4ac982e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929848"
---
# <span data-ttu-id="8985a-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="8985a-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="8985a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8985a-102">SYNOPSIS</span></span>
<span data-ttu-id="8985a-103">Ruft eine Aktion für eine Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="8985a-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="8985a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8985a-104">SYNTAX</span></span>

### <span data-ttu-id="8985a-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="8985a-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8985a-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="8985a-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8985a-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="8985a-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8985a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8985a-108">DESCRIPTION</span></span>
<span data-ttu-id="8985a-109">Das **Cmdlet Invoke-AzResourceAction** ruft eine Aktion für eine angegebene Azure-Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="8985a-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="8985a-110">Verwenden Sie das Azure-Ressourcen-Explorer-Tool, um eine Liste der unterstützten Aktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8985a-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="8985a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8985a-111">EXAMPLES</span></span>

### <span data-ttu-id="8985a-112">Beispiel 1: Aufrufen des Startens einer VM mit ResourceId</span><span class="sxs-lookup"><span data-stu-id="8985a-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="8985a-113">Mit diesem Befehl wird der virtuelle Computer mit {ResourceId} gestartet.</span><span class="sxs-lookup"><span data-stu-id="8985a-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="8985a-114">Beispiel 2: Aufrufen des Poweroffings einer VM mit ResourceName</span><span class="sxs-lookup"><span data-stu-id="8985a-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="8985a-115">Mit diesem Befehl wird der virtuelle Computer mit {ResourceId} beendet.</span><span class="sxs-lookup"><span data-stu-id="8985a-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="8985a-116">Der Befehl gibt den *Parameter Erzwingen* an, daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8985a-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8985a-117">Beispiel 3: Aufrufen der Registrierung eines Ressourcenanbieters mit ResourceId</span><span class="sxs-lookup"><span data-stu-id="8985a-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="8985a-118">Mit diesem Befehl wird der Ressourcenanbieter "Microsoft.Network" registriert.</span><span class="sxs-lookup"><span data-stu-id="8985a-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="8985a-119">Der Befehl gibt den *Parameter Erzwingen* an, daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8985a-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8985a-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8985a-120">PARAMETERS</span></span>

### <span data-ttu-id="8985a-121">-Aktion</span><span class="sxs-lookup"><span data-stu-id="8985a-121">-Action</span></span>
<span data-ttu-id="8985a-122">Gibt den Namen der aktion an, die aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8985a-122">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8985a-123">-ApiVersion</span></span>
<span data-ttu-id="8985a-124">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="8985a-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8985a-125">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="8985a-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8985a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8985a-126">-DefaultProfile</span></span>
<span data-ttu-id="8985a-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8985a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8985a-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="8985a-128">-ExtensionResourceName</span></span>
<span data-ttu-id="8985a-129">Gibt den Namen einer Erweiterungsressource für die Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="8985a-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="8985a-130">Verwenden Sie beispielsweise zum Angeben einer Datenbank das folgende Format: Name `/` der Servernamedatenbank</span><span class="sxs-lookup"><span data-stu-id="8985a-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="8985a-131">-ExtensionResourceType</span></span>
<span data-ttu-id="8985a-132">Gibt den Typ der Erweiterungsressource an.</span><span class="sxs-lookup"><span data-stu-id="8985a-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="8985a-133">Zum Beispiel: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="8985a-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-134">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="8985a-134">-Force</span></span>
<span data-ttu-id="8985a-135">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="8985a-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8985a-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8985a-136">-ODataQuery</span></span>
<span data-ttu-id="8985a-137">Gibt einen OData-Stilfilter (Open Data Protocol) an.</span><span class="sxs-lookup"><span data-stu-id="8985a-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="8985a-138">Dieses Cmdlet fügt diesen Wert zusätzlich zu allen anderen Filtern an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="8985a-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="8985a-139">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8985a-139">-Parameters</span></span>
<span data-ttu-id="8985a-140">Gibt Parameter als Hashtabelle für die Aktion an, die von diesem Cmdlet aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8985a-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="8985a-141">-Pre</span></span>
<span data-ttu-id="8985a-142">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8985a-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8985a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8985a-143">-ResourceGroupName</span></span>
<span data-ttu-id="8985a-144">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="8985a-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8985a-145">-ResourceId</span></span>
<span data-ttu-id="8985a-146">Gibt die vollqualifizierte Ressourcen-ID der Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="8985a-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="8985a-147">Die ID enthält das Abonnement, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8985a-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8985a-148">-ResourceName</span></span>
<span data-ttu-id="8985a-149">Gibt den Namen der Ressource der Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="8985a-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="8985a-150">Um beispielsweise eine Datenbank anzugeben, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8985a-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8985a-151">-ResourceType</span></span>
<span data-ttu-id="8985a-152">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="8985a-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="8985a-153">Für eine Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="8985a-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8985a-154">-TenantLevel</span></span>
<span data-ttu-id="8985a-155">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8985a-155">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8985a-156">-Confirm</span></span>
<span data-ttu-id="8985a-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8985a-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8985a-158">-WhatIf</span></span>
<span data-ttu-id="8985a-159">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8985a-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8985a-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8985a-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8985a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8985a-161">CommonParameters</span></span>
<span data-ttu-id="8985a-162">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8985a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8985a-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8985a-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8985a-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8985a-164">INPUTS</span></span>

### <span data-ttu-id="8985a-165">System.String</span><span class="sxs-lookup"><span data-stu-id="8985a-165">System.String</span></span>

## <span data-ttu-id="8985a-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8985a-166">OUTPUTS</span></span>

### <span data-ttu-id="8985a-167">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8985a-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8985a-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8985a-168">NOTES</span></span>

## <span data-ttu-id="8985a-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8985a-169">RELATED LINKS</span></span>

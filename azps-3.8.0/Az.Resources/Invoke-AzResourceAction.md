---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2feb6c48927c1cb5e092414c358b32912892a908
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003982"
---
# <span data-ttu-id="f2e82-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="f2e82-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="f2e82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2e82-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e82-103">Ruft eine Aktion für eine Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="f2e82-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="f2e82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2e82-104">SYNTAX</span></span>

### <span data-ttu-id="f2e82-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2e82-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2e82-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f2e82-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2e82-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f2e82-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2e82-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2e82-108">DESCRIPTION</span></span>
<span data-ttu-id="f2e82-109">Das Cmdlet **Invoke-AzResourceAction** Ruft eine Aktion für eine angegebene Azure-Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="f2e82-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="f2e82-110">Verwenden Sie zum Abrufen einer Liste unterstützter Aktionen das Azure Resource Explorer-Tool.</span><span class="sxs-lookup"><span data-stu-id="f2e82-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="f2e82-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2e82-111">EXAMPLES</span></span>

### <span data-ttu-id="f2e82-112">Beispiel 1: Aufrufen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="f2e82-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="f2e82-113">Mit diesem Befehl wird der virtuelle Computer mit {resourcecode} gestartet.</span><span class="sxs-lookup"><span data-stu-id="f2e82-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="f2e82-114">Beispiel 2: Aufrufen von poweroffing einer VM mit resourceName</span><span class="sxs-lookup"><span data-stu-id="f2e82-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="f2e82-115">Dieser Befehl beendet den virtuellen Computer mit {Resourcen-Nr.}.</span><span class="sxs-lookup"><span data-stu-id="f2e82-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="f2e82-116">Der Befehl gibt den Parameter *Force* an, daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="f2e82-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="f2e82-117">Beispiel 3: Aufrufen der Registrierung eines Ressourcenanbieters mit der Ressourcenquelle</span><span class="sxs-lookup"><span data-stu-id="f2e82-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

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

<span data-ttu-id="f2e82-118">Mit diesem Befehl wird ein Ressourcenanbieter "Microsoft. Network" registriert.</span><span class="sxs-lookup"><span data-stu-id="f2e82-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="f2e82-119">Der Befehl gibt den Parameter *Force* an, daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="f2e82-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f2e82-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2e82-120">PARAMETERS</span></span>

### <span data-ttu-id="f2e82-121">– Aktion</span><span class="sxs-lookup"><span data-stu-id="f2e82-121">-Action</span></span>
<span data-ttu-id="f2e82-122">Gibt den Namen der aufzurufenden Aktion an.</span><span class="sxs-lookup"><span data-stu-id="f2e82-122">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="f2e82-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f2e82-123">-ApiVersion</span></span>
<span data-ttu-id="f2e82-124">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="f2e82-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f2e82-125">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="f2e82-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f2e82-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e82-126">-DefaultProfile</span></span>
<span data-ttu-id="f2e82-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f2e82-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2e82-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="f2e82-128">-ExtensionResourceName</span></span>
<span data-ttu-id="f2e82-129">Gibt den Namen einer Erweiterungs Ressource für die Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="f2e82-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="f2e82-130">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Servername- `/` Datenbankname</span><span class="sxs-lookup"><span data-stu-id="f2e82-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="f2e82-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="f2e82-131">-ExtensionResourceType</span></span>
<span data-ttu-id="f2e82-132">Gibt den Typ der Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="f2e82-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="f2e82-133">Zum Beispiel: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="f2e82-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="f2e82-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f2e82-134">-Force</span></span>
<span data-ttu-id="f2e82-135">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f2e82-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f2e82-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="f2e82-136">-ODataQuery</span></span>
<span data-ttu-id="f2e82-137">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="f2e82-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="f2e82-138">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="f2e82-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="f2e82-139">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f2e82-139">-Parameters</span></span>
<span data-ttu-id="f2e82-140">Gibt Parameter als Hashtabelle für die Aktion an, die von diesem Cmdlet aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f2e82-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="f2e82-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="f2e82-141">-Pre</span></span>
<span data-ttu-id="f2e82-142">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f2e82-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f2e82-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2e82-143">-ResourceGroupName</span></span>
<span data-ttu-id="f2e82-144">Gibt den Namen einer Ressourcengruppe an, in der mit diesem Cmdlet eine Aktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f2e82-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="f2e82-145">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f2e82-145">-ResourceId</span></span>
<span data-ttu-id="f2e82-146">Gibt die vollqualifizierte Ressourcen-ID der Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="f2e82-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="f2e82-147">Die ID enthält das Abonnement, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f2e82-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="f2e82-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f2e82-148">-ResourceName</span></span>
<span data-ttu-id="f2e82-149">Gibt den Namen der Ressource der Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="f2e82-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="f2e82-150">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f2e82-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="f2e82-151">-</span><span class="sxs-lookup"><span data-stu-id="f2e82-151">-ResourceType</span></span>
<span data-ttu-id="f2e82-152">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="f2e82-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="f2e82-153">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="f2e82-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="f2e82-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f2e82-154">-TenantLevel</span></span>
<span data-ttu-id="f2e82-155">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f2e82-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="f2e82-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2e82-156">-Confirm</span></span>
<span data-ttu-id="f2e82-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2e82-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2e82-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e82-158">-WhatIf</span></span>
<span data-ttu-id="f2e82-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2e82-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2e82-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2e82-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2e82-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e82-161">CommonParameters</span></span>
<span data-ttu-id="f2e82-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e82-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e82-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2e82-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e82-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2e82-164">INPUTS</span></span>

### <span data-ttu-id="f2e82-165">System. String</span><span class="sxs-lookup"><span data-stu-id="f2e82-165">System.String</span></span>

## <span data-ttu-id="f2e82-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2e82-166">OUTPUTS</span></span>

### <span data-ttu-id="f2e82-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f2e82-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f2e82-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2e82-168">NOTES</span></span>

## <span data-ttu-id="f2e82-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2e82-169">RELATED LINKS</span></span>

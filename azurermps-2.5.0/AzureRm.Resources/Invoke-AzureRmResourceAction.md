---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
ms.openlocfilehash: e29dda3fc5d2b62196d0cc5897ba7a7c9b047a8c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849912"
---
# <span data-ttu-id="538a6-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="538a6-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="538a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="538a6-102">SYNOPSIS</span></span>
<span data-ttu-id="538a6-103">Ruft eine Aktion für eine Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="538a6-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="538a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="538a6-104">SYNTAX</span></span>

### <span data-ttu-id="538a6-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="538a6-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="538a6-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="538a6-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="538a6-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="538a6-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="538a6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="538a6-108">DESCRIPTION</span></span>
<span data-ttu-id="538a6-109">Das Cmdlet **Invoke-AzureRmResourceAction** Ruft eine Aktion für eine angegebene Azure-Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="538a6-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="538a6-110">Verwenden Sie zum Abrufen einer Liste unterstützter Aktionen das Azure Resource Explorer-Tool.</span><span class="sxs-lookup"><span data-stu-id="538a6-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="538a6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="538a6-111">EXAMPLES</span></span>

## <span data-ttu-id="538a6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="538a6-112">PARAMETERS</span></span>

### <span data-ttu-id="538a6-113">– Aktion</span><span class="sxs-lookup"><span data-stu-id="538a6-113">-Action</span></span>
<span data-ttu-id="538a6-114">Gibt den Namen der aufzurufenden Aktion an.</span><span class="sxs-lookup"><span data-stu-id="538a6-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="538a6-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="538a6-115">-ApiVersion</span></span>
<span data-ttu-id="538a6-116">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="538a6-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="538a6-117">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="538a6-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="538a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="538a6-118">-DefaultProfile</span></span>
<span data-ttu-id="538a6-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="538a6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="538a6-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="538a6-120">-ExtensionResourceName</span></span>
<span data-ttu-id="538a6-121">Gibt den Namen einer Erweiterungs Ressource für die Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="538a6-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="538a6-122">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Servername- `/` Datenbankname</span><span class="sxs-lookup"><span data-stu-id="538a6-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="538a6-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="538a6-123">-ExtensionResourceType</span></span>
<span data-ttu-id="538a6-124">Gibt den Typ der Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="538a6-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="538a6-125">Zum Beispiel: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="538a6-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="538a6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="538a6-126">-Force</span></span>
<span data-ttu-id="538a6-127">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="538a6-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="538a6-128">-Information</span><span class="sxs-lookup"><span data-stu-id="538a6-128">-InformationAction</span></span>
<span data-ttu-id="538a6-129">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="538a6-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="538a6-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="538a6-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="538a6-131">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="538a6-131">Continue</span></span>
- <span data-ttu-id="538a6-132">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="538a6-132">Ignore</span></span>
- <span data-ttu-id="538a6-133">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="538a6-133">Inquire</span></span>
- <span data-ttu-id="538a6-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="538a6-134">SilentlyContinue</span></span>
- <span data-ttu-id="538a6-135">Beenden</span><span class="sxs-lookup"><span data-stu-id="538a6-135">Stop</span></span>
- <span data-ttu-id="538a6-136">Anhalten</span><span class="sxs-lookup"><span data-stu-id="538a6-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="538a6-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="538a6-137">-InformationVariable</span></span>
<span data-ttu-id="538a6-138">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="538a6-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="538a6-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="538a6-139">-ODataQuery</span></span>
<span data-ttu-id="538a6-140">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="538a6-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="538a6-141">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="538a6-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="538a6-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="538a6-142">-Parameters</span></span>
<span data-ttu-id="538a6-143">Gibt Parameter als Hashtabelle für die Aktion an, die von diesem Cmdlet aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="538a6-143">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="538a6-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="538a6-144">-Pre</span></span>
<span data-ttu-id="538a6-145">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="538a6-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="538a6-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="538a6-146">-ResourceGroupName</span></span>
<span data-ttu-id="538a6-147">Gibt den Namen einer Ressourcengruppe an, in der mit diesem Cmdlet eine Aktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="538a6-147">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="538a6-148">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="538a6-148">-ResourceId</span></span>
<span data-ttu-id="538a6-149">Gibt die vollqualifizierte Ressourcen-ID der Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="538a6-149">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="538a6-150">Die ID enthält das Abonnement, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="538a6-150">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="538a6-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="538a6-151">-ResourceName</span></span>
<span data-ttu-id="538a6-152">Gibt den Namen der Ressource der Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="538a6-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="538a6-153">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="538a6-153">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="538a6-154">-</span><span class="sxs-lookup"><span data-stu-id="538a6-154">-ResourceType</span></span>
<span data-ttu-id="538a6-155">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="538a6-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="538a6-156">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="538a6-156">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="538a6-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="538a6-157">-TenantLevel</span></span>
<span data-ttu-id="538a6-158">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="538a6-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="538a6-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="538a6-159">-Confirm</span></span>
<span data-ttu-id="538a6-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="538a6-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="538a6-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="538a6-161">-WhatIf</span></span>
<span data-ttu-id="538a6-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="538a6-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="538a6-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="538a6-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="538a6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="538a6-164">CommonParameters</span></span>
<span data-ttu-id="538a6-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="538a6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="538a6-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="538a6-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="538a6-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="538a6-167">INPUTS</span></span>

## <span data-ttu-id="538a6-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="538a6-168">OUTPUTS</span></span>

## <span data-ttu-id="538a6-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="538a6-169">NOTES</span></span>

## <span data-ttu-id="538a6-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="538a6-170">RELATED LINKS</span></span>

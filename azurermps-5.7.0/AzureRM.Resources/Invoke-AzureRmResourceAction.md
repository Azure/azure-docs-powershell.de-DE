---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 7f2aa8299e3e4dcbdc6d326dfedf76092a65f351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663439"
---
# <span data-ttu-id="9af15-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="9af15-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="9af15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9af15-102">SYNOPSIS</span></span>
<span data-ttu-id="9af15-103">Ruft eine Aktion für eine Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="9af15-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9af15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9af15-104">SYNTAX</span></span>

### <span data-ttu-id="9af15-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="9af15-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9af15-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="9af15-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9af15-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9af15-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9af15-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9af15-108">DESCRIPTION</span></span>
<span data-ttu-id="9af15-109">Das Cmdlet **Invoke-AzureRmResourceAction** Ruft eine Aktion für eine angegebene Azure-Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="9af15-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="9af15-110">Verwenden Sie zum Abrufen einer Liste unterstützter Aktionen das Azure Resource Explorer-Tool.</span><span class="sxs-lookup"><span data-stu-id="9af15-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="9af15-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9af15-111">EXAMPLES</span></span>

## <span data-ttu-id="9af15-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9af15-112">PARAMETERS</span></span>

### <span data-ttu-id="9af15-113">– Aktion</span><span class="sxs-lookup"><span data-stu-id="9af15-113">-Action</span></span>
<span data-ttu-id="9af15-114">Gibt den Namen der aufzurufenden Aktion an.</span><span class="sxs-lookup"><span data-stu-id="9af15-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9af15-115">-ApiVersion</span></span>
<span data-ttu-id="9af15-116">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="9af15-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9af15-117">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="9af15-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af15-118">-DefaultProfile</span></span>
<span data-ttu-id="9af15-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9af15-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="9af15-120">-ExtensionResourceName</span></span>
<span data-ttu-id="9af15-121">Gibt den Namen einer Erweiterungs Ressource für die Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="9af15-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="9af15-122">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="9af15-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="9af15-123">Name der Servernamen- `/` Datenbank</span><span class="sxs-lookup"><span data-stu-id="9af15-123">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="9af15-124">-ExtensionResourceType</span></span>
<span data-ttu-id="9af15-125">Gibt den Typ der Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="9af15-125">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="9af15-126">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9af15-126">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9af15-127">-Force</span></span>
<span data-ttu-id="9af15-128">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9af15-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-129">-Information</span><span class="sxs-lookup"><span data-stu-id="9af15-129">-InformationAction</span></span>
<span data-ttu-id="9af15-130">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="9af15-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9af15-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9af15-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9af15-132">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="9af15-132">Continue</span></span>
- <span data-ttu-id="9af15-133">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="9af15-133">Ignore</span></span>
- <span data-ttu-id="9af15-134">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="9af15-134">Inquire</span></span>
- <span data-ttu-id="9af15-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9af15-135">SilentlyContinue</span></span>
- <span data-ttu-id="9af15-136">Beenden</span><span class="sxs-lookup"><span data-stu-id="9af15-136">Stop</span></span>
- <span data-ttu-id="9af15-137">Anhalten</span><span class="sxs-lookup"><span data-stu-id="9af15-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9af15-138">-InformationVariable</span></span>
<span data-ttu-id="9af15-139">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="9af15-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-140">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9af15-140">-ODataQuery</span></span>
<span data-ttu-id="9af15-141">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="9af15-141">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="9af15-142">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="9af15-142">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-143">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9af15-143">-Parameters</span></span>
<span data-ttu-id="9af15-144">Gibt Parameter als Hashtabelle für die Aktion an, die von diesem Cmdlet aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9af15-144">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="9af15-145">-Pre</span></span>
<span data-ttu-id="9af15-146">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="9af15-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af15-147">-ResourceGroupName</span></span>
<span data-ttu-id="9af15-148">Gibt den Namen einer Ressourcengruppe an, in der mit diesem Cmdlet eine Aktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9af15-148">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-149">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9af15-149">-ResourceId</span></span>
<span data-ttu-id="9af15-150">Gibt die vollqualifizierte Ressourcen-ID der Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="9af15-150">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="9af15-151">Die ID enthält das Abonnement, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9af15-151">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="9af15-152">`/subscriptions/`Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9af15-152">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9af15-153">-ResourceName</span></span>
<span data-ttu-id="9af15-154">Gibt den Namen der Ressource der Ressource an, für die dieses Cmdlet eine Aktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="9af15-154">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="9af15-155">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="9af15-155">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-156">-</span><span class="sxs-lookup"><span data-stu-id="9af15-156">-ResourceType</span></span>
<span data-ttu-id="9af15-157">Gibt den Typ der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="9af15-157">Specifies the type of the resource.</span></span>
<span data-ttu-id="9af15-158">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9af15-158">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9af15-159">-TenantLevel</span></span>
<span data-ttu-id="9af15-160">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9af15-160">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9af15-161">-Confirm</span></span>
<span data-ttu-id="9af15-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9af15-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9af15-163">-WhatIf</span></span>
<span data-ttu-id="9af15-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9af15-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9af15-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9af15-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af15-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af15-166">CommonParameters</span></span>
<span data-ttu-id="9af15-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af15-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af15-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af15-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af15-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9af15-169">INPUTS</span></span>

### <span data-ttu-id="9af15-170">Keine</span><span class="sxs-lookup"><span data-stu-id="9af15-170">None</span></span>
<span data-ttu-id="9af15-171">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9af15-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9af15-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9af15-172">OUTPUTS</span></span>

### <span data-ttu-id="9af15-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9af15-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9af15-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="9af15-174">NOTES</span></span>

## <span data-ttu-id="9af15-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9af15-175">RELATED LINKS</span></span>

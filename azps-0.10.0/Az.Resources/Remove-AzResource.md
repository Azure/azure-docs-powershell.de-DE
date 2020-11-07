---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: b8560e867204265b23c459a7019044173983c301
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "93851047"
---
# <span data-ttu-id="b6dc2-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="b6dc2-101">Remove-AzResource</span></span>

## <span data-ttu-id="b6dc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6dc2-103">Entfernt eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-103">Removes a resource.</span></span>

## <span data-ttu-id="b6dc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6dc2-104">SYNTAX</span></span>

### <span data-ttu-id="b6dc2-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6dc2-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6dc2-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="b6dc2-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6dc2-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="b6dc2-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6dc2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6dc2-108">DESCRIPTION</span></span>
<span data-ttu-id="b6dc2-109">Das Cmdlet **Remove-AzResource** entfernt eine Azure-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="b6dc2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6dc2-110">EXAMPLES</span></span>

### <span data-ttu-id="b6dc2-111">Beispiel 1: Entfernen einer Website Ressource</span><span class="sxs-lookup"><span data-stu-id="b6dc2-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="b6dc2-112">Dieser Befehl entfernt die Website Ressource mit dem Namen ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="b6dc2-113">Im Beispiel wird ein Platzhalterwert für die Abonnement-ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="b6dc2-114">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b6dc2-115">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b6dc2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6dc2-116">PARAMETERS</span></span>

### <span data-ttu-id="b6dc2-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b6dc2-117">-ApiVersion</span></span>
<span data-ttu-id="b6dc2-118">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b6dc2-119">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b6dc2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6dc2-120">-AsJob</span></span>
<span data-ttu-id="b6dc2-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b6dc2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6dc2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6dc2-122">-DefaultProfile</span></span>
<span data-ttu-id="b6dc2-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b6dc2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6dc2-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="b6dc2-124">-ExtensionResourceName</span></span>
<span data-ttu-id="b6dc2-125">Gibt den Namen einer Erweiterungs Ressource der Ressource an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b6dc2-126">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: Servername- `/` Datenbankname</span><span class="sxs-lookup"><span data-stu-id="b6dc2-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="b6dc2-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="b6dc2-127">-ExtensionResourceType</span></span>
<span data-ttu-id="b6dc2-128">Gibt den Ressourcentyp für eine Erweiterungs Ressource an.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="b6dc2-129">Gibt den Erweiterungs Ressourcentyp für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="b6dc2-130">Zum Beispiel: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="b6dc2-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="b6dc2-131">-Force</span><span class="sxs-lookup"><span data-stu-id="b6dc2-131">-Force</span></span>
<span data-ttu-id="b6dc2-132">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6dc2-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b6dc2-133">-ODataQuery</span></span>
<span data-ttu-id="b6dc2-134">Gibt einen Open Data Protocol (OData)-stilfilter an.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="b6dc2-135">Dieses Cmdlet fügt zusätzlich zu anderen Filtern diesen Wert an die Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="b6dc2-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="b6dc2-136">-Pre</span></span>
<span data-ttu-id="b6dc2-137">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b6dc2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6dc2-138">-ResourceGroupName</span></span>
<span data-ttu-id="b6dc2-139">Gibt den Namen der Ressourcengruppe an, aus der das Cmdlet eine Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="b6dc2-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b6dc2-140">-ResourceId</span></span>
<span data-ttu-id="b6dc2-141">Gibt die vollqualifizierte Ressourcen-ID der Ressource an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b6dc2-142">Die ID enthält das Abonnement, wie im folgenden Beispiel: `/subscriptions/` Abonnement-ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b6dc2-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="b6dc2-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b6dc2-143">-ResourceName</span></span>
<span data-ttu-id="b6dc2-144">Gibt den Namen der Ressource an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b6dc2-145">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b6dc2-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="b6dc2-146">-</span><span class="sxs-lookup"><span data-stu-id="b6dc2-146">-ResourceType</span></span>
<span data-ttu-id="b6dc2-147">Gibt den Typ der Ressource an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="b6dc2-148">Bei einer Datenbank lautet der Ressourcentyp beispielsweise wie folgt: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="b6dc2-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="b6dc2-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b6dc2-149">-TenantLevel</span></span>
<span data-ttu-id="b6dc2-150">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="b6dc2-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b6dc2-151">-Confirm</span></span>
<span data-ttu-id="b6dc2-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6dc2-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6dc2-153">-WhatIf</span></span>
<span data-ttu-id="b6dc2-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6dc2-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6dc2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6dc2-156">CommonParameters</span></span>
<span data-ttu-id="b6dc2-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6dc2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6dc2-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6dc2-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6dc2-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6dc2-159">INPUTS</span></span>

### <span data-ttu-id="b6dc2-160">Keine</span><span class="sxs-lookup"><span data-stu-id="b6dc2-160">None</span></span>

## <span data-ttu-id="b6dc2-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6dc2-161">OUTPUTS</span></span>

### <span data-ttu-id="b6dc2-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6dc2-162">System.Boolean</span></span>

## <span data-ttu-id="b6dc2-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6dc2-163">NOTES</span></span>

## <span data-ttu-id="b6dc2-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6dc2-164">RELATED LINKS</span></span>

[<span data-ttu-id="b6dc2-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="b6dc2-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="b6dc2-166">Verschieben-AzResource</span><span class="sxs-lookup"><span data-stu-id="b6dc2-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="b6dc2-167">Neu – AzResource</span><span class="sxs-lookup"><span data-stu-id="b6dc2-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="b6dc2-168">Satz-AzResource</span><span class="sxs-lookup"><span data-stu-id="b6dc2-168">Set-AzResource</span></span>](./Set-AzResource.md)



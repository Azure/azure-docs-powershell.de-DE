---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: 355de1e4eb4518b8ec3d7291b20f76bda5fb1a89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920123"
---
# <span data-ttu-id="9e3ec-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="9e3ec-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="9e3ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3ec-103">Erstellen und Ausführen einer HTTP-Anforderung nur an Azure-Ressourcenverwaltungsendpunkt</span><span class="sxs-lookup"><span data-stu-id="9e3ec-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="9e3ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e3ec-104">SYNTAX</span></span>

### <span data-ttu-id="9e3ec-105">ByPath (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e3ec-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e3ec-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="9e3ec-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e3ec-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e3ec-107">DESCRIPTION</span></span>
<span data-ttu-id="9e3ec-108">Erstellen und Ausführen einer HTTP-Anforderung nur an Azure-Ressourcenverwaltungsendpunkt</span><span class="sxs-lookup"><span data-stu-id="9e3ec-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="9e3ec-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e3ec-109">EXAMPLES</span></span>

### <span data-ttu-id="9e3ec-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e3ec-110">Example 1</span></span>
```powershell
Invoke-AzRestMethod -Path "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}?api-version={API}" -Method GET

Headers    : {[Cache-Control, System.String[]], [Pragma, System.String[]], [x-ms-request-id, System.String[]], [Strict-Transport-Security, System.String[]]…}
Version    : 1.1
StatusCode : 200
Method     : GET
Content    : {
               "properties": {
                 "source": "Azure",
                 "customerId": "{customerId}",
                 "provisioningState": "Succeeded",
                 "sku": {
                   "name": "pergb2018",
                   "maxCapacityReservationLevel": 3000,
                   "lastSkuUpdate": "Mon, 25 May 2020 11:10:01 GMT"
                 },
                 "retentionInDays": 30,
                 "features": {
                   "legacy": 0,
                   "searchVersion": 1,
                   "enableLogAccessUsingOnlyResourcePermissions": true
                 },
                 "workspaceCapping": {
                   "dailyQuotaGb": -1.0,
                   "quotaNextResetTime": "Thu, 18 Jun 2020 05:00:00 GMT",
                   "dataIngestionStatus": "RespectQuota"
                 },
                 "enableFailover": false,
                 "publicNetworkAccessForIngestion": "Enabled",
                 "publicNetworkAccessForQuery": "Enabled",
                 "createdDate": "Mon, 25 May 2020 11:10:01 GMT",
                 "modifiedDate": "Mon, 25 May 2020 11:10:02 GMT"
               },
               "id": "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}",
               "name": "{workspace}",
               "type": "Microsoft.OperationalInsights/workspaces",
               "location": "eastasia",
               "tags": {}
             }
```

<span data-ttu-id="9e3ec-111">Protokollanalysearbeitsbereich nach Pfad erhalten</span><span class="sxs-lookup"><span data-stu-id="9e3ec-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="9e3ec-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9e3ec-112">PARAMETERS</span></span>

### <span data-ttu-id="9e3ec-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9e3ec-113">-ApiVersion</span></span>
<span data-ttu-id="9e3ec-114">Api-Version</span><span class="sxs-lookup"><span data-stu-id="9e3ec-114">Api Version</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3ec-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e3ec-115">-AsJob</span></span>
<span data-ttu-id="9e3ec-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9e3ec-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e3ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3ec-117">-DefaultProfile</span></span>
<span data-ttu-id="9e3ec-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e3ec-119">-Methode</span><span class="sxs-lookup"><span data-stu-id="9e3ec-119">-Method</span></span>
<span data-ttu-id="9e3ec-120">Http-Methode</span><span class="sxs-lookup"><span data-stu-id="9e3ec-120">Http Method</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3ec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9e3ec-121">-Name</span></span>
<span data-ttu-id="9e3ec-122">Liste des Zielressourcennamens</span><span class="sxs-lookup"><span data-stu-id="9e3ec-122">list of Target Resource Name</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3ec-123">-Path</span><span class="sxs-lookup"><span data-stu-id="9e3ec-123">-Path</span></span>
<span data-ttu-id="9e3ec-124">Zielpfad</span><span class="sxs-lookup"><span data-stu-id="9e3ec-124">Target Path</span></span>

```yaml
Type: System.String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3ec-125">-Payload</span><span class="sxs-lookup"><span data-stu-id="9e3ec-125">-Payload</span></span>
<span data-ttu-id="9e3ec-126">Nutzlast im JSON-Format</span><span class="sxs-lookup"><span data-stu-id="9e3ec-126">JSON format payload</span></span>

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

### <span data-ttu-id="9e3ec-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e3ec-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e3ec-128">Name der Zielressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9e3ec-128">Target Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3ec-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="9e3ec-129">-ResourceProviderName</span></span>
<span data-ttu-id="9e3ec-130">Name des Zielressourcenanbieters</span><span class="sxs-lookup"><span data-stu-id="9e3ec-130">Target Resource Provider Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3ec-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9e3ec-131">-ResourceType</span></span>
<span data-ttu-id="9e3ec-132">Liste des Zielressourcentyps</span><span class="sxs-lookup"><span data-stu-id="9e3ec-132">List of Target Resource Type</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3ec-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e3ec-133">-SubscriptionId</span></span>
<span data-ttu-id="9e3ec-134">Zielabonnement-ID</span><span class="sxs-lookup"><span data-stu-id="9e3ec-134">Target Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3ec-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e3ec-135">-Confirm</span></span>
<span data-ttu-id="9e3ec-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e3ec-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e3ec-137">-WhatIf</span></span>
<span data-ttu-id="9e3ec-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e3ec-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e3ec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3ec-140">CommonParameters</span></span>
<span data-ttu-id="9e3ec-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3ec-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e3ec-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3ec-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e3ec-143">INPUTS</span></span>

### <span data-ttu-id="9e3ec-144">System.string</span><span class="sxs-lookup"><span data-stu-id="9e3ec-144">System.string</span></span>

## <span data-ttu-id="9e3ec-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e3ec-145">OUTPUTS</span></span>

### <span data-ttu-id="9e3ec-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="9e3ec-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="9e3ec-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9e3ec-147">NOTES</span></span>

## <span data-ttu-id="9e3ec-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9e3ec-148">RELATED LINKS</span></span>

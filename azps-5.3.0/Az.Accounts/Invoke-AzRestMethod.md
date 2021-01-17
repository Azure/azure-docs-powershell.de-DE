---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469195"
---
# <span data-ttu-id="aebca-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="aebca-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="aebca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aebca-102">SYNOPSIS</span></span>
<span data-ttu-id="aebca-103">Erstellen und Ausführen einer HTTP-Anforderung nur an den Azure-Ressourcenverwaltungsendpunkt</span><span class="sxs-lookup"><span data-stu-id="aebca-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="aebca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aebca-104">SYNTAX</span></span>

### <span data-ttu-id="aebca-105">ByPath (Standard)</span><span class="sxs-lookup"><span data-stu-id="aebca-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aebca-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="aebca-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aebca-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aebca-107">DESCRIPTION</span></span>
<span data-ttu-id="aebca-108">Erstellen und Ausführen einer HTTP-Anforderung nur an den Azure-Ressourcenverwaltungsendpunkt</span><span class="sxs-lookup"><span data-stu-id="aebca-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="aebca-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aebca-109">EXAMPLES</span></span>

### <span data-ttu-id="aebca-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aebca-110">Example 1</span></span>
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

<span data-ttu-id="aebca-111">Zugreifen auf den Protokollanalysearbeitsbereich nach Pfad</span><span class="sxs-lookup"><span data-stu-id="aebca-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="aebca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aebca-112">PARAMETERS</span></span>

### <span data-ttu-id="aebca-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aebca-113">-ApiVersion</span></span>
<span data-ttu-id="aebca-114">API-Version</span><span class="sxs-lookup"><span data-stu-id="aebca-114">Api Version</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aebca-115">-AsJob</span></span>
<span data-ttu-id="aebca-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="aebca-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aebca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aebca-117">-DefaultProfile</span></span>
<span data-ttu-id="aebca-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aebca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-119">-Methode</span><span class="sxs-lookup"><span data-stu-id="aebca-119">-Method</span></span>
<span data-ttu-id="aebca-120">Http-Methode</span><span class="sxs-lookup"><span data-stu-id="aebca-120">Http Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-121">-Name</span><span class="sxs-lookup"><span data-stu-id="aebca-121">-Name</span></span>
<span data-ttu-id="aebca-122">Liste des Zielressourcennamens</span><span class="sxs-lookup"><span data-stu-id="aebca-122">list of Target Resource Name</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-123">-Path</span><span class="sxs-lookup"><span data-stu-id="aebca-123">-Path</span></span>
<span data-ttu-id="aebca-124">Zielpfad</span><span class="sxs-lookup"><span data-stu-id="aebca-124">Target Path</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-125">-Payload</span><span class="sxs-lookup"><span data-stu-id="aebca-125">-Payload</span></span>
<span data-ttu-id="aebca-126">Nutzlast des JSON-Formats</span><span class="sxs-lookup"><span data-stu-id="aebca-126">JSON format payload</span></span>

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

### <span data-ttu-id="aebca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aebca-127">-ResourceGroupName</span></span>
<span data-ttu-id="aebca-128">Name der Zielressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="aebca-128">Target Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="aebca-129">-ResourceProviderName</span></span>
<span data-ttu-id="aebca-130">Name des Zielressourcenanbieters</span><span class="sxs-lookup"><span data-stu-id="aebca-130">Target Resource Provider Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="aebca-131">-ResourceType</span></span>
<span data-ttu-id="aebca-132">Liste des Zielressourcentyps</span><span class="sxs-lookup"><span data-stu-id="aebca-132">List of Target Resource Type</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aebca-133">-SubscriptionId</span></span>
<span data-ttu-id="aebca-134">Zielabonnement-ID</span><span class="sxs-lookup"><span data-stu-id="aebca-134">Target Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aebca-135">-Confirm</span></span>
<span data-ttu-id="aebca-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aebca-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aebca-137">-WhatIf</span></span>
<span data-ttu-id="aebca-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aebca-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aebca-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aebca-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aebca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aebca-140">CommonParameters</span></span>
<span data-ttu-id="aebca-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aebca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aebca-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aebca-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aebca-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aebca-143">INPUTS</span></span>

### <span data-ttu-id="aebca-144">System.string</span><span class="sxs-lookup"><span data-stu-id="aebca-144">System.string</span></span>

## <span data-ttu-id="aebca-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aebca-145">OUTPUTS</span></span>

### <span data-ttu-id="aebca-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="aebca-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="aebca-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aebca-147">NOTES</span></span>

## <span data-ttu-id="aebca-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aebca-148">RELATED LINKS</span></span>

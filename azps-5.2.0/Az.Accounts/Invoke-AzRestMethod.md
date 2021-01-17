---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363906"
---
# <span data-ttu-id="a70d3-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="a70d3-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="a70d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a70d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a70d3-103">Erstellen und Ausführen einer HTTP-Anforderung nur an den Azure-Ressourcenverwaltungsendpunkt</span><span class="sxs-lookup"><span data-stu-id="a70d3-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="a70d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a70d3-104">SYNTAX</span></span>

### <span data-ttu-id="a70d3-105">ByPath (Standard)</span><span class="sxs-lookup"><span data-stu-id="a70d3-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a70d3-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="a70d3-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a70d3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a70d3-107">DESCRIPTION</span></span>
<span data-ttu-id="a70d3-108">Erstellen und Ausführen einer HTTP-Anforderung nur an den Azure-Ressourcenverwaltungsendpunkt</span><span class="sxs-lookup"><span data-stu-id="a70d3-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="a70d3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a70d3-109">EXAMPLES</span></span>

### <span data-ttu-id="a70d3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a70d3-110">Example 1</span></span>
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

<span data-ttu-id="a70d3-111">Zugreifen auf den Loganalysearbeitsbereich nach Pfad</span><span class="sxs-lookup"><span data-stu-id="a70d3-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="a70d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a70d3-112">PARAMETERS</span></span>

### <span data-ttu-id="a70d3-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a70d3-113">-ApiVersion</span></span>
<span data-ttu-id="a70d3-114">API-Version</span><span class="sxs-lookup"><span data-stu-id="a70d3-114">Api Version</span></span>

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

### <span data-ttu-id="a70d3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a70d3-115">-AsJob</span></span>
<span data-ttu-id="a70d3-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a70d3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a70d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70d3-117">-DefaultProfile</span></span>
<span data-ttu-id="a70d3-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a70d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a70d3-119">-Methode</span><span class="sxs-lookup"><span data-stu-id="a70d3-119">-Method</span></span>
<span data-ttu-id="a70d3-120">Http-Methode</span><span class="sxs-lookup"><span data-stu-id="a70d3-120">Http Method</span></span>

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

### <span data-ttu-id="a70d3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a70d3-121">-Name</span></span>
<span data-ttu-id="a70d3-122">Liste des Zielressourcennamens</span><span class="sxs-lookup"><span data-stu-id="a70d3-122">list of Target Resource Name</span></span>

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

### <span data-ttu-id="a70d3-123">-Path</span><span class="sxs-lookup"><span data-stu-id="a70d3-123">-Path</span></span>
<span data-ttu-id="a70d3-124">Zielpfad</span><span class="sxs-lookup"><span data-stu-id="a70d3-124">Target Path</span></span>

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

### <span data-ttu-id="a70d3-125">-Payload</span><span class="sxs-lookup"><span data-stu-id="a70d3-125">-Payload</span></span>
<span data-ttu-id="a70d3-126">Nutzlast des JSON-Formats</span><span class="sxs-lookup"><span data-stu-id="a70d3-126">JSON format payload</span></span>

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

### <span data-ttu-id="a70d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="a70d3-128">Name der Zielressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a70d3-128">Target Resource Group Name</span></span>

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

### <span data-ttu-id="a70d3-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="a70d3-129">-ResourceProviderName</span></span>
<span data-ttu-id="a70d3-130">Name des Zielressourcenanbieters</span><span class="sxs-lookup"><span data-stu-id="a70d3-130">Target Resource Provider Name</span></span>

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

### <span data-ttu-id="a70d3-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a70d3-131">-ResourceType</span></span>
<span data-ttu-id="a70d3-132">Liste des Zielressourcentyps</span><span class="sxs-lookup"><span data-stu-id="a70d3-132">List of Target Resource Type</span></span>

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

### <span data-ttu-id="a70d3-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a70d3-133">-SubscriptionId</span></span>
<span data-ttu-id="a70d3-134">Zielabonnement-ID</span><span class="sxs-lookup"><span data-stu-id="a70d3-134">Target Subscription Id</span></span>

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

### <span data-ttu-id="a70d3-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a70d3-135">-Confirm</span></span>
<span data-ttu-id="a70d3-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a70d3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a70d3-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a70d3-137">-WhatIf</span></span>
<span data-ttu-id="a70d3-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a70d3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a70d3-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a70d3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a70d3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70d3-140">CommonParameters</span></span>
<span data-ttu-id="a70d3-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a70d3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70d3-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a70d3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70d3-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a70d3-143">INPUTS</span></span>

### <span data-ttu-id="a70d3-144">System.string</span><span class="sxs-lookup"><span data-stu-id="a70d3-144">System.string</span></span>

## <span data-ttu-id="a70d3-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a70d3-145">OUTPUTS</span></span>

### <span data-ttu-id="a70d3-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="a70d3-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="a70d3-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a70d3-147">NOTES</span></span>

## <span data-ttu-id="a70d3-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a70d3-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929128"
---
# <span data-ttu-id="ead9e-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="ead9e-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="ead9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ead9e-102">SYNOPSIS</span></span>
<span data-ttu-id="ead9e-103">Unformatiertes Zugriffstoken erhalten.</span><span class="sxs-lookup"><span data-stu-id="ead9e-103">Get raw access token.</span></span> <span data-ttu-id="ead9e-104">Stellen Sie bei Verwendung von -ResourceUrl sicher, dass der Wert der aktuellen Azure-Umgebung zu entsprechen hat.</span><span class="sxs-lookup"><span data-stu-id="ead9e-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="ead9e-105">Sie können auf den Wert von `(Get-AzContext).Environment` verweisen.</span><span class="sxs-lookup"><span data-stu-id="ead9e-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="ead9e-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ead9e-106">SYNTAX</span></span>

### <span data-ttu-id="ead9e-107">KnownResourceTypeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ead9e-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ead9e-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="ead9e-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ead9e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ead9e-109">DESCRIPTION</span></span>
<span data-ttu-id="ead9e-110">Zugriffstoken erhalten</span><span class="sxs-lookup"><span data-stu-id="ead9e-110">Get access token</span></span>

## <span data-ttu-id="ead9e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ead9e-111">EXAMPLES</span></span>

### <span data-ttu-id="ead9e-112">Beispiel 1 Unformatiertes Zugriffstoken für ARM Endpunkt</span><span class="sxs-lookup"><span data-stu-id="ead9e-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="ead9e-113">Zugriffstoken des ResourceManager-Endpunkts für das aktuelle Konto erhalten</span><span class="sxs-lookup"><span data-stu-id="ead9e-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="ead9e-114">Beispiel 2 Unformatiertes Zugriffstoken für AAD-Diagrammendpunkt</span><span class="sxs-lookup"><span data-stu-id="ead9e-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="ead9e-115">Zugriffstoken des AAD-Diagrammendpunkts für das aktuelle Konto</span><span class="sxs-lookup"><span data-stu-id="ead9e-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="ead9e-116">Beispiel 3 Unformatiertes Zugriffstoken für AAD-Diagrammendpunkt</span><span class="sxs-lookup"><span data-stu-id="ead9e-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="ead9e-117">Zugriffstoken des AAD-Diagrammendpunkts für das aktuelle Konto</span><span class="sxs-lookup"><span data-stu-id="ead9e-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="ead9e-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ead9e-118">PARAMETERS</span></span>

### <span data-ttu-id="ead9e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead9e-119">-DefaultProfile</span></span>
<span data-ttu-id="ead9e-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ead9e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead9e-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="ead9e-121">-ResourceTypeName</span></span>
<span data-ttu-id="ead9e-122">Optional: Typname neu erstellen, unterstützte Werte: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="ead9e-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="ead9e-123">Standardwert ist Arm, wenn nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="ead9e-123">Default value is Arm if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead9e-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="ead9e-124">-ResourceUrl</span></span>
<span data-ttu-id="ead9e-125">Ressourcen-URL für das Token, das Sie anfordern, z. B. ' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="ead9e-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead9e-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ead9e-126">-TenantId</span></span>
<span data-ttu-id="ead9e-127">Optionale Mandanten-ID. Verwenden Sie die Mandanten-ID des Standardkontexts, wenn sie nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ead9e-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="ead9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead9e-128">CommonParameters</span></span>
<span data-ttu-id="ead9e-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead9e-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ead9e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead9e-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ead9e-131">INPUTS</span></span>

### <span data-ttu-id="ead9e-132">Keine</span><span class="sxs-lookup"><span data-stu-id="ead9e-132">None</span></span>

## <span data-ttu-id="ead9e-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ead9e-133">OUTPUTS</span></span>

### <span data-ttu-id="ead9e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ead9e-134">System.String</span></span>

## <span data-ttu-id="ead9e-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ead9e-135">NOTES</span></span>

## <span data-ttu-id="ead9e-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ead9e-136">RELATED LINKS</span></span>

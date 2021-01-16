---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294335"
---
# <span data-ttu-id="7177f-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="7177f-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="7177f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7177f-102">SYNOPSIS</span></span>
<span data-ttu-id="7177f-103">Token für den unformatierte Zugriff</span><span class="sxs-lookup"><span data-stu-id="7177f-103">Get raw access token.</span></span> <span data-ttu-id="7177f-104">Stellen Sie bei Verwendung von "-ResourceUrl" sicher, dass der Wert mit der aktuellen Azure-Umgebung übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="7177f-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="7177f-105">Sie können auf den Wert von `(Get-AzContext).Environment` verweisen.</span><span class="sxs-lookup"><span data-stu-id="7177f-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="7177f-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7177f-106">SYNTAX</span></span>

### <span data-ttu-id="7177f-107">KnownResourceTypeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7177f-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7177f-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="7177f-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7177f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7177f-109">DESCRIPTION</span></span>
<span data-ttu-id="7177f-110">Zugriffstoken erhalten</span><span class="sxs-lookup"><span data-stu-id="7177f-110">Get access token</span></span>

## <span data-ttu-id="7177f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7177f-111">EXAMPLES</span></span>

### <span data-ttu-id="7177f-112">Beispiel 1: Token für den unformatierte Zugriff für ARM Endpunkt</span><span class="sxs-lookup"><span data-stu-id="7177f-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="7177f-113">Zugriffstoken des ResourceManager-Endpunkts für aktuelles Konto erhalten</span><span class="sxs-lookup"><span data-stu-id="7177f-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="7177f-114">Beispiel 2: Token für den unformatierte Zugriff für den AAD-Diagrammendpunkt</span><span class="sxs-lookup"><span data-stu-id="7177f-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="7177f-115">Zugriffstoken des AAD -Diagrammendpunkts für aktuelles Konto erhalten</span><span class="sxs-lookup"><span data-stu-id="7177f-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="7177f-116">Beispiel 3: Token für den unformatierte Zugriff für den AAD-Diagrammendpunkt</span><span class="sxs-lookup"><span data-stu-id="7177f-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="7177f-117">Zugriffstoken des AAD -Diagrammendpunkts für aktuelles Konto erhalten</span><span class="sxs-lookup"><span data-stu-id="7177f-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="7177f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7177f-118">PARAMETERS</span></span>

### <span data-ttu-id="7177f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7177f-119">-DefaultProfile</span></span>
<span data-ttu-id="7177f-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7177f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7177f-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="7177f-121">-ResourceTypeName</span></span>
<span data-ttu-id="7177f-122">Name des optionalen Typs, unterstützte Werte: AadGraph, AnalysisServices, Arm, Nachweis, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="7177f-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="7177f-123">Der Standardwert ist "Arm", wenn dieser nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7177f-123">Default value is Arm if not specified.</span></span>

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

### <span data-ttu-id="7177f-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="7177f-124">-ResourceUrl</span></span>
<span data-ttu-id="7177f-125">Ressourcen-URL für das Token, das Sie anfordern, z. B. ' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="7177f-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

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

### <span data-ttu-id="7177f-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7177f-126">-TenantId</span></span>
<span data-ttu-id="7177f-127">Optionale Mandanten-ID. Verwenden Sie die Mandanten-ID des Standardkontexts, wenn dieser nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7177f-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="7177f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7177f-128">CommonParameters</span></span>
<span data-ttu-id="7177f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7177f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7177f-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7177f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7177f-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7177f-131">INPUTS</span></span>

### <span data-ttu-id="7177f-132">Keine</span><span class="sxs-lookup"><span data-stu-id="7177f-132">None</span></span>

## <span data-ttu-id="7177f-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7177f-133">OUTPUTS</span></span>

### <span data-ttu-id="7177f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7177f-134">System.String</span></span>

## <span data-ttu-id="7177f-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7177f-135">NOTES</span></span>

## <span data-ttu-id="7177f-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7177f-136">RELATED LINKS</span></span>

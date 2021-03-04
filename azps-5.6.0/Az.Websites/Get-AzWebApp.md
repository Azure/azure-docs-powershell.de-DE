---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 32e71b33b3c440701e501c4b68d740dcf121001d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934555"
---
# <span data-ttu-id="8427a-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8427a-101">Get-AzWebApp</span></span>

## <span data-ttu-id="8427a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8427a-102">SYNOPSIS</span></span>
<span data-ttu-id="8427a-103">Ruft Azure Web Apps in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8427a-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="8427a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8427a-104">SYNTAX</span></span>

### <span data-ttu-id="8427a-105">S1</span><span class="sxs-lookup"><span data-stu-id="8427a-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8427a-106">S2</span><span class="sxs-lookup"><span data-stu-id="8427a-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8427a-107">S3</span><span class="sxs-lookup"><span data-stu-id="8427a-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8427a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8427a-108">DESCRIPTION</span></span>
<span data-ttu-id="8427a-109">Das **Get-AzWebApp-Cmdlet** ruft Informationen zu einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="8427a-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="8427a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8427a-110">EXAMPLES</span></span>

### <span data-ttu-id="8427a-111">Beispiel 1: Herunterladen einer Web App aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8427a-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="8427a-112">Dieser Befehl ruft die Web App mit dem Namen ContosoSite ab, die zur Ressourcengruppe Default-Web-WestUS gehört.</span><span class="sxs-lookup"><span data-stu-id="8427a-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8427a-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8427a-113">PARAMETERS</span></span>

### <span data-ttu-id="8427a-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8427a-114">-AppServicePlan</span></span>
<span data-ttu-id="8427a-115">App Service Plan-Objekt</span><span class="sxs-lookup"><span data-stu-id="8427a-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8427a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8427a-116">-DefaultProfile</span></span>
<span data-ttu-id="8427a-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8427a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8427a-118">-Location</span><span class="sxs-lookup"><span data-stu-id="8427a-118">-Location</span></span>
<span data-ttu-id="8427a-119">Ort</span><span class="sxs-lookup"><span data-stu-id="8427a-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8427a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8427a-120">-Name</span></span>
<span data-ttu-id="8427a-121">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="8427a-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8427a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8427a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8427a-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8427a-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8427a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8427a-124">CommonParameters</span></span>
<span data-ttu-id="8427a-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8427a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8427a-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8427a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8427a-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8427a-127">INPUTS</span></span>

### <span data-ttu-id="8427a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8427a-128">System.String</span></span>

## <span data-ttu-id="8427a-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8427a-129">OUTPUTS</span></span>

### <span data-ttu-id="8427a-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8427a-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8427a-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8427a-131">NOTES</span></span>

## <span data-ttu-id="8427a-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8427a-132">RELATED LINKS</span></span>

[<span data-ttu-id="8427a-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8427a-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="8427a-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8427a-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="8427a-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8427a-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="8427a-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8427a-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="8427a-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8427a-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



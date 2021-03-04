---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 102dbd678fe6fe46034a43c46cb713428b8564d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948136"
---
# <span data-ttu-id="a4aa8-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a4aa8-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="a4aa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="a4aa8-103">Beendet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="a4aa8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4aa8-104">SYNTAX</span></span>

### <span data-ttu-id="a4aa8-105">S1</span><span class="sxs-lookup"><span data-stu-id="a4aa8-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4aa8-106">S2</span><span class="sxs-lookup"><span data-stu-id="a4aa8-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4aa8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4aa8-107">DESCRIPTION</span></span>
<span data-ttu-id="a4aa8-108">Das **Cmdlet Stop-AzWebApp** beendet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="a4aa8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4aa8-109">EXAMPLES</span></span>

### <span data-ttu-id="a4aa8-110">Beispiel 1: Beenden einer Web App</span><span class="sxs-lookup"><span data-stu-id="a4aa8-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a4aa8-111">Mit diesem Befehl wird die Web App mit dem Namen ContosoWebApp beendet, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a4aa8-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a4aa8-112">PARAMETERS</span></span>

### <span data-ttu-id="a4aa8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4aa8-113">-DefaultProfile</span></span>
<span data-ttu-id="a4aa8-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4aa8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a4aa8-115">-Name</span></span>
<span data-ttu-id="a4aa8-116">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="a4aa8-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4aa8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4aa8-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4aa8-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a4aa8-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4aa8-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a4aa8-119">-WebApp</span></span>
<span data-ttu-id="a4aa8-120">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="a4aa8-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4aa8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4aa8-121">CommonParameters</span></span>
<span data-ttu-id="a4aa8-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4aa8-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4aa8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4aa8-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4aa8-124">INPUTS</span></span>

### <span data-ttu-id="a4aa8-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a4aa8-125">System.String</span></span>

### <span data-ttu-id="a4aa8-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a4aa8-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a4aa8-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4aa8-127">OUTPUTS</span></span>

### <span data-ttu-id="a4aa8-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a4aa8-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a4aa8-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a4aa8-129">NOTES</span></span>

## <span data-ttu-id="a4aa8-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a4aa8-130">RELATED LINKS</span></span>

[<span data-ttu-id="a4aa8-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a4aa8-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a4aa8-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a4aa8-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a4aa8-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a4aa8-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a4aa8-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a4aa8-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a4aa8-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a4aa8-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



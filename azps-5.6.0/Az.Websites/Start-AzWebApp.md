---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: a05b9ef015d1685e92bc56b0056c9213ff3370ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948160"
---
# <span data-ttu-id="ec970-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec970-101">Start-AzWebApp</span></span>

## <span data-ttu-id="ec970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec970-102">SYNOPSIS</span></span>
<span data-ttu-id="ec970-103">Startet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ec970-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="ec970-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec970-104">SYNTAX</span></span>

### <span data-ttu-id="ec970-105">S1</span><span class="sxs-lookup"><span data-stu-id="ec970-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec970-106">S2</span><span class="sxs-lookup"><span data-stu-id="ec970-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec970-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec970-107">DESCRIPTION</span></span>
<span data-ttu-id="ec970-108">Das **Cmdlet Start-AzWebApp** startet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ec970-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="ec970-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec970-109">EXAMPLES</span></span>

### <span data-ttu-id="ec970-110">Beispiel 1: Starten einer Web App</span><span class="sxs-lookup"><span data-stu-id="ec970-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="ec970-111">Mit diesem Befehl wird die Web App namens ContosoWebApp gestartet, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="ec970-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ec970-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ec970-112">PARAMETERS</span></span>

### <span data-ttu-id="ec970-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec970-113">-DefaultProfile</span></span>
<span data-ttu-id="ec970-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec970-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec970-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ec970-115">-Name</span></span>
<span data-ttu-id="ec970-116">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="ec970-116">WebApp Name</span></span>

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

### <span data-ttu-id="ec970-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec970-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec970-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ec970-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ec970-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ec970-119">-WebApp</span></span>
<span data-ttu-id="ec970-120">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="ec970-120">WebApp Object</span></span>

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

### <span data-ttu-id="ec970-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec970-121">CommonParameters</span></span>
<span data-ttu-id="ec970-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec970-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec970-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec970-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec970-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec970-124">INPUTS</span></span>

### <span data-ttu-id="ec970-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ec970-125">System.String</span></span>

### <span data-ttu-id="ec970-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ec970-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ec970-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec970-127">OUTPUTS</span></span>

### <span data-ttu-id="ec970-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ec970-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ec970-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ec970-129">NOTES</span></span>

## <span data-ttu-id="ec970-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ec970-130">RELATED LINKS</span></span>

[<span data-ttu-id="ec970-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec970-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ec970-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec970-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ec970-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec970-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ec970-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec970-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ec970-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ec970-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



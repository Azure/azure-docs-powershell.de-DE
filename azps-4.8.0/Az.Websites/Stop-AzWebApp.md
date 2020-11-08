---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174857"
---
# <span data-ttu-id="ced21-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ced21-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="ced21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ced21-102">SYNOPSIS</span></span>
<span data-ttu-id="ced21-103">Beendet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ced21-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="ced21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ced21-104">SYNTAX</span></span>

### <span data-ttu-id="ced21-105">S1</span><span class="sxs-lookup"><span data-stu-id="ced21-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ced21-106">S2</span><span class="sxs-lookup"><span data-stu-id="ced21-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ced21-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ced21-107">DESCRIPTION</span></span>
<span data-ttu-id="ced21-108">Das Cmdlet **Stop-AzWebApp** beendet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ced21-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="ced21-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ced21-109">EXAMPLES</span></span>

### <span data-ttu-id="ced21-110">Beispiel 1: Beenden einer Web-App</span><span class="sxs-lookup"><span data-stu-id="ced21-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="ced21-111">Mit diesem Befehl wird die Web-App mit dem Namen ContosoWebApp beendet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="ced21-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ced21-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ced21-112">PARAMETERS</span></span>

### <span data-ttu-id="ced21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced21-113">-DefaultProfile</span></span>
<span data-ttu-id="ced21-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ced21-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ced21-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ced21-115">-Name</span></span>
<span data-ttu-id="ced21-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="ced21-116">WebApp Name</span></span>

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

### <span data-ttu-id="ced21-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced21-117">-ResourceGroupName</span></span>
<span data-ttu-id="ced21-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ced21-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ced21-119">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="ced21-119">-WebApp</span></span>
<span data-ttu-id="ced21-120">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="ced21-120">WebApp Object</span></span>

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

### <span data-ttu-id="ced21-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced21-121">CommonParameters</span></span>
<span data-ttu-id="ced21-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced21-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced21-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ced21-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced21-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ced21-124">INPUTS</span></span>

### <span data-ttu-id="ced21-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ced21-125">System.String</span></span>

### <span data-ttu-id="ced21-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ced21-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ced21-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ced21-127">OUTPUTS</span></span>

### <span data-ttu-id="ced21-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ced21-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ced21-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ced21-129">NOTES</span></span>

## <span data-ttu-id="ced21-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ced21-130">RELATED LINKS</span></span>

[<span data-ttu-id="ced21-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ced21-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ced21-132">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ced21-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ced21-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ced21-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ced21-134">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ced21-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ced21-135">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ced21-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



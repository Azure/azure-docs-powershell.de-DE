---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: b389a84ea57902e2e7a7dabaea2d853827a728e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477529"
---
# <span data-ttu-id="ff1d5-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff1d5-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="ff1d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff1d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1d5-103">Beendet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ff1d5-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff1d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff1d5-104">SYNTAX</span></span>

### <span data-ttu-id="ff1d5-105">S1</span><span class="sxs-lookup"><span data-stu-id="ff1d5-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff1d5-106">S2</span><span class="sxs-lookup"><span data-stu-id="ff1d5-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff1d5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff1d5-107">DESCRIPTION</span></span>
<span data-ttu-id="ff1d5-108">Das Cmdlet **Stop-AzureRmWebApp** beendet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ff1d5-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="ff1d5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff1d5-109">EXAMPLES</span></span>

### <span data-ttu-id="ff1d5-110">Beispiel 1: Beenden einer Web-App</span><span class="sxs-lookup"><span data-stu-id="ff1d5-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="ff1d5-111">Mit diesem Befehl wird die Web-App mit dem Namen ContosoWebApp beendet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="ff1d5-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ff1d5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff1d5-112">PARAMETERS</span></span>

### <span data-ttu-id="ff1d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff1d5-113">-DefaultProfile</span></span>
<span data-ttu-id="ff1d5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff1d5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1d5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ff1d5-115">-Name</span></span>
<span data-ttu-id="ff1d5-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="ff1d5-116">WebApp Name</span></span>

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

### <span data-ttu-id="ff1d5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff1d5-117">-ResourceGroupName</span></span>
<span data-ttu-id="ff1d5-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ff1d5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ff1d5-119">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="ff1d5-119">-WebApp</span></span>
<span data-ttu-id="ff1d5-120">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="ff1d5-120">WebApp Object</span></span>

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

### <span data-ttu-id="ff1d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1d5-121">CommonParameters</span></span>
<span data-ttu-id="ff1d5-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff1d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1d5-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff1d5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1d5-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff1d5-124">INPUTS</span></span>

### <span data-ttu-id="ff1d5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ff1d5-125">System.String</span></span>

### <span data-ttu-id="ff1d5-126">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="ff1d5-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="ff1d5-127">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="ff1d5-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="ff1d5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff1d5-128">OUTPUTS</span></span>

### <span data-ttu-id="ff1d5-129">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="ff1d5-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="ff1d5-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff1d5-130">NOTES</span></span>

## <span data-ttu-id="ff1d5-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff1d5-131">RELATED LINKS</span></span>

[<span data-ttu-id="ff1d5-132">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff1d5-132">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="ff1d5-133">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff1d5-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="ff1d5-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff1d5-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="ff1d5-135">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff1d5-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="ff1d5-136">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ff1d5-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)



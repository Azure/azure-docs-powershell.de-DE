---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 20acba9bc0f08857c9bdfaaf559544f26b4902ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477094"
---
# <span data-ttu-id="fb46d-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fb46d-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="fb46d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb46d-102">SYNOPSIS</span></span>
<span data-ttu-id="fb46d-103">Startet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fb46d-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb46d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb46d-104">SYNTAX</span></span>

### <span data-ttu-id="fb46d-105">S1</span><span class="sxs-lookup"><span data-stu-id="fb46d-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb46d-106">S2</span><span class="sxs-lookup"><span data-stu-id="fb46d-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb46d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb46d-107">DESCRIPTION</span></span>
<span data-ttu-id="fb46d-108">Das Cmdlet **Start-AzureRmWebApp** startet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fb46d-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="fb46d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb46d-109">EXAMPLES</span></span>

### <span data-ttu-id="fb46d-110">Beispiel 1: Starten einer Web-App</span><span class="sxs-lookup"><span data-stu-id="fb46d-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="fb46d-111">Mit diesem Befehl wird die Web-App mit dem Namen ContosoWebApp gestartet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="fb46d-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="fb46d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb46d-112">PARAMETERS</span></span>

### <span data-ttu-id="fb46d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fb46d-113">-Name</span></span>
<span data-ttu-id="fb46d-114">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="fb46d-114">WebApp Name</span></span>

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

### <span data-ttu-id="fb46d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb46d-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb46d-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="fb46d-116">Resource Group Name</span></span>

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

### <span data-ttu-id="fb46d-117">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="fb46d-117">-WebApp</span></span>
<span data-ttu-id="fb46d-118">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="fb46d-118">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb46d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb46d-119">-DefaultProfile</span></span>
<span data-ttu-id="fb46d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb46d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb46d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb46d-121">CommonParameters</span></span>
<span data-ttu-id="fb46d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb46d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb46d-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb46d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb46d-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb46d-124">INPUTS</span></span>

### <span data-ttu-id="fb46d-125">Website</span><span class="sxs-lookup"><span data-stu-id="fb46d-125">Site</span></span>
<span data-ttu-id="fb46d-126">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fb46d-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fb46d-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb46d-127">OUTPUTS</span></span>

## <span data-ttu-id="fb46d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb46d-128">NOTES</span></span>

## <span data-ttu-id="fb46d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb46d-129">RELATED LINKS</span></span>

[<span data-ttu-id="fb46d-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fb46d-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="fb46d-131">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fb46d-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="fb46d-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fb46d-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="fb46d-133">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fb46d-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="fb46d-134">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="fb46d-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)



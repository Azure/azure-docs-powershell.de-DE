---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 0e1c1b9a2aa20546db1306b47b54b18c2b0cd99e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849860"
---
# <span data-ttu-id="479e6-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="479e6-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="479e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="479e6-102">SYNOPSIS</span></span>
<span data-ttu-id="479e6-103">Beendet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="479e6-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="479e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="479e6-104">SYNTAX</span></span>

### <span data-ttu-id="479e6-105">S1</span><span class="sxs-lookup"><span data-stu-id="479e6-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="479e6-106">S2</span><span class="sxs-lookup"><span data-stu-id="479e6-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="479e6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="479e6-107">DESCRIPTION</span></span>
<span data-ttu-id="479e6-108">Das Cmdlet **Stop-AzureRmWebApp** beendet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="479e6-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="479e6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="479e6-109">EXAMPLES</span></span>

### <span data-ttu-id="479e6-110">Beispiel 1: Beenden einer Web-App</span><span class="sxs-lookup"><span data-stu-id="479e6-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="479e6-111">Mit diesem Befehl wird die Web-App mit dem Namen ContosoWebApp beendet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="479e6-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="479e6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="479e6-112">PARAMETERS</span></span>

### <span data-ttu-id="479e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="479e6-113">-DefaultProfile</span></span>
<span data-ttu-id="479e6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="479e6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479e6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="479e6-115">-Name</span></span>
<span data-ttu-id="479e6-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="479e6-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479e6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="479e6-117">-ResourceGroupName</span></span>
<span data-ttu-id="479e6-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="479e6-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479e6-119">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="479e6-119">-WebApp</span></span>
<span data-ttu-id="479e6-120">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="479e6-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="479e6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="479e6-121">CommonParameters</span></span>
<span data-ttu-id="479e6-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="479e6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="479e6-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="479e6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="479e6-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="479e6-124">INPUTS</span></span>

### <span data-ttu-id="479e6-125">Website</span><span class="sxs-lookup"><span data-stu-id="479e6-125">Site</span></span>
<span data-ttu-id="479e6-126">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="479e6-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="479e6-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="479e6-127">OUTPUTS</span></span>

## <span data-ttu-id="479e6-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="479e6-128">NOTES</span></span>

## <span data-ttu-id="479e6-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="479e6-129">RELATED LINKS</span></span>

[<span data-ttu-id="479e6-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="479e6-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="479e6-131">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="479e6-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="479e6-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="479e6-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="479e6-133">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="479e6-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="479e6-134">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="479e6-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)



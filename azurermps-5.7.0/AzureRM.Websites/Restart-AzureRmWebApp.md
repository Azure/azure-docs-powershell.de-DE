---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: 7543a1dfbbab0c2cedc59fd8ca0d3b60d78ca69d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662338"
---
# <span data-ttu-id="474b1-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="474b1-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="474b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="474b1-102">SYNOPSIS</span></span>
<span data-ttu-id="474b1-103">Startet eine Azure Web App neu.</span><span class="sxs-lookup"><span data-stu-id="474b1-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="474b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="474b1-104">SYNTAX</span></span>

### <span data-ttu-id="474b1-105">S1</span><span class="sxs-lookup"><span data-stu-id="474b1-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="474b1-106">S2</span><span class="sxs-lookup"><span data-stu-id="474b1-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="474b1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="474b1-107">DESCRIPTION</span></span>
<span data-ttu-id="474b1-108">Das Cmdlet " **Restart-AzureRmWebApp** " beendet und startet dann eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="474b1-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="474b1-109">Wenn sich die Web-App im Zustand "beendet" befindet, verwenden Sie das Cmdlet "Start-AzureRmWebApp".</span><span class="sxs-lookup"><span data-stu-id="474b1-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="474b1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="474b1-110">EXAMPLES</span></span>

### <span data-ttu-id="474b1-111">Beispiel 1: Erneutes Starten einer Web-App</span><span class="sxs-lookup"><span data-stu-id="474b1-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="474b1-112">Mit diesem Befehl wird die Azure Web App mit dem Namen ContosoSite beendet, die zu der Ressourcengruppe Default-Web-westus gehört und dann neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="474b1-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="474b1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="474b1-113">PARAMETERS</span></span>

### <span data-ttu-id="474b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474b1-114">-DefaultProfile</span></span>
<span data-ttu-id="474b1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="474b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="474b1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="474b1-116">-Name</span></span>
<span data-ttu-id="474b1-117">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="474b1-117">WebApp Name</span></span>

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

### <span data-ttu-id="474b1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474b1-118">-ResourceGroupName</span></span>
<span data-ttu-id="474b1-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="474b1-119">Resource Group Name</span></span>

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

### <span data-ttu-id="474b1-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="474b1-120">-WebApp</span></span>
<span data-ttu-id="474b1-121">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="474b1-121">WebApp Object</span></span>

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

### <span data-ttu-id="474b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474b1-122">CommonParameters</span></span>
<span data-ttu-id="474b1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="474b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474b1-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474b1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474b1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="474b1-125">INPUTS</span></span>

### <span data-ttu-id="474b1-126">Website</span><span class="sxs-lookup"><span data-stu-id="474b1-126">Site</span></span>
<span data-ttu-id="474b1-127">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="474b1-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="474b1-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="474b1-128">OUTPUTS</span></span>

## <span data-ttu-id="474b1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="474b1-129">NOTES</span></span>

## <span data-ttu-id="474b1-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="474b1-130">RELATED LINKS</span></span>

[<span data-ttu-id="474b1-131">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="474b1-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="474b1-132">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="474b1-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="474b1-133">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="474b1-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="474b1-134">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="474b1-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="474b1-135">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="474b1-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)



---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: f082241be9e31b11782fcbbf5570a7f3c3947012
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848051"
---
# <span data-ttu-id="c1577-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c1577-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="c1577-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1577-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1577-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1577-103">SYNTAX</span></span>

### <span data-ttu-id="c1577-104">S1</span><span class="sxs-lookup"><span data-stu-id="c1577-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1577-105">S2</span><span class="sxs-lookup"><span data-stu-id="c1577-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1577-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1577-106">DESCRIPTION</span></span>
<span data-ttu-id="c1577-107">Das Cmdlet **Reset-AzureRmWebAppPublishingProfile** setzt das Veröffentlichungsprofil für die angegebene Web-App zurück.</span><span class="sxs-lookup"><span data-stu-id="c1577-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="c1577-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1577-108">EXAMPLES</span></span>

### <span data-ttu-id="c1577-109">1:</span><span class="sxs-lookup"><span data-stu-id="c1577-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="c1577-110">Mit diesem Befehl wird das Veröffentlichungsprofil für das Web-App-ContosoWebApp zurückgesetzt, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c1577-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c1577-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1577-111">PARAMETERS</span></span>

### <span data-ttu-id="c1577-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1577-112">-DefaultProfile</span></span>
<span data-ttu-id="c1577-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1577-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1577-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c1577-114">-Name</span></span>
<span data-ttu-id="c1577-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="c1577-115">WebApp Name</span></span>

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

### <span data-ttu-id="c1577-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1577-116">-ResourceGroupName</span></span>
<span data-ttu-id="c1577-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c1577-117">Resource Group Name</span></span>

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

### <span data-ttu-id="c1577-118">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="c1577-118">-WebApp</span></span>
<span data-ttu-id="c1577-119">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="c1577-119">WebApp Object</span></span>

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

### <span data-ttu-id="c1577-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1577-120">CommonParameters</span></span>
<span data-ttu-id="c1577-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1577-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1577-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1577-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1577-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1577-123">INPUTS</span></span>

### <span data-ttu-id="c1577-124">Website</span><span class="sxs-lookup"><span data-stu-id="c1577-124">Site</span></span>
<span data-ttu-id="c1577-125">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1577-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c1577-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1577-126">OUTPUTS</span></span>

## <span data-ttu-id="c1577-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1577-127">NOTES</span></span>

## <span data-ttu-id="c1577-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1577-128">RELATED LINKS</span></span>


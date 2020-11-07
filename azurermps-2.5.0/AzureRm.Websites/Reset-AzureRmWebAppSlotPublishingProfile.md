---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 7c385f230456da60df76c56fc652dda53362c778
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850531"
---
# <span data-ttu-id="623b8-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="623b8-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="623b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="623b8-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="623b8-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="623b8-103">SYNTAX</span></span>

### <span data-ttu-id="623b8-104">S1</span><span class="sxs-lookup"><span data-stu-id="623b8-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="623b8-105">S2</span><span class="sxs-lookup"><span data-stu-id="623b8-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="623b8-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="623b8-106">DESCRIPTION</span></span>
<span data-ttu-id="623b8-107">Das Cmdlet **Reset-AzureRmWebAppSlotPublishingProfile** setzt das Veröffentlichungsprofil für den angegebenen Web App-Slot zurück.</span><span class="sxs-lookup"><span data-stu-id="623b8-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="623b8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="623b8-108">EXAMPLES</span></span>

### <span data-ttu-id="623b8-109">1:</span><span class="sxs-lookup"><span data-stu-id="623b8-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="623b8-110">Mit diesem Befehl wird das Veröffentlichungsprofil für den Steckplatz mit dem Namen slot001 für das Web-App-ContosoWebApp zurückgesetzt, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="623b8-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="623b8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="623b8-111">PARAMETERS</span></span>

### <span data-ttu-id="623b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623b8-112">-DefaultProfile</span></span>
<span data-ttu-id="623b8-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="623b8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="623b8-114">-Name</span><span class="sxs-lookup"><span data-stu-id="623b8-114">-Name</span></span>
<span data-ttu-id="623b8-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="623b8-115">WebApp Name</span></span>

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

### <span data-ttu-id="623b8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="623b8-116">-ResourceGroupName</span></span>
<span data-ttu-id="623b8-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="623b8-117">Resource Group Name</span></span>

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

### <span data-ttu-id="623b8-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="623b8-118">-Slot</span></span>
<span data-ttu-id="623b8-119">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="623b8-119">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623b8-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="623b8-120">-WebApp</span></span>
<span data-ttu-id="623b8-121">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="623b8-121">WebApp Object</span></span>

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

### <span data-ttu-id="623b8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623b8-122">CommonParameters</span></span>
<span data-ttu-id="623b8-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623b8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623b8-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="623b8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623b8-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="623b8-125">INPUTS</span></span>

### <span data-ttu-id="623b8-126">Website</span><span class="sxs-lookup"><span data-stu-id="623b8-126">Site</span></span>
<span data-ttu-id="623b8-127">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="623b8-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="623b8-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="623b8-128">OUTPUTS</span></span>

## <span data-ttu-id="623b8-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="623b8-129">NOTES</span></span>

## <span data-ttu-id="623b8-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="623b8-130">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: c59e40765fc5da07c5d079e3b5abd6224a8cbc5f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849855"
---
# <span data-ttu-id="467c4-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="467c4-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="467c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="467c4-102">SYNOPSIS</span></span>
<span data-ttu-id="467c4-103">Beendet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="467c4-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="467c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="467c4-104">SYNTAX</span></span>

### <span data-ttu-id="467c4-105">S1</span><span class="sxs-lookup"><span data-stu-id="467c4-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="467c4-106">S2</span><span class="sxs-lookup"><span data-stu-id="467c4-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="467c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="467c4-107">DESCRIPTION</span></span>
<span data-ttu-id="467c4-108">Das Cmdlet **Stop-AzureRmWebAppSlot** beendet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="467c4-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="467c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="467c4-109">EXAMPLES</span></span>

### <span data-ttu-id="467c4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="467c4-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="467c4-111">Mit diesem Befehl wird der Slot Slot001 in Bezug auf die Web-App mit dem Namen ContosoWebApp, die zu der Ressourcengruppe Default-Web-westus gehört, beendet.</span><span class="sxs-lookup"><span data-stu-id="467c4-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="467c4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="467c4-112">PARAMETERS</span></span>

### <span data-ttu-id="467c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467c4-113">-DefaultProfile</span></span>
<span data-ttu-id="467c4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="467c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="467c4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="467c4-115">-Name</span></span>
<span data-ttu-id="467c4-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="467c4-116">WebApp Name</span></span>

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

### <span data-ttu-id="467c4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="467c4-117">-ResourceGroupName</span></span>
<span data-ttu-id="467c4-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="467c4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="467c4-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="467c4-119">-Slot</span></span>
<span data-ttu-id="467c4-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="467c4-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="467c4-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="467c4-121">-WebApp</span></span>
<span data-ttu-id="467c4-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="467c4-122">WebApp Object</span></span>

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

### <span data-ttu-id="467c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467c4-123">CommonParameters</span></span>
<span data-ttu-id="467c4-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="467c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467c4-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="467c4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467c4-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="467c4-126">INPUTS</span></span>

### <span data-ttu-id="467c4-127">Website</span><span class="sxs-lookup"><span data-stu-id="467c4-127">Site</span></span>
<span data-ttu-id="467c4-128">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="467c4-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="467c4-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="467c4-129">OUTPUTS</span></span>

## <span data-ttu-id="467c4-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="467c4-130">NOTES</span></span>

## <span data-ttu-id="467c4-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="467c4-131">RELATED LINKS</span></span>


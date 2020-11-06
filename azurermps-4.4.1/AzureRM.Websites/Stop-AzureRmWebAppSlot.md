---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 91a8c53bc8600006a3a57a5dfefb1141652ca3d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477086"
---
# <span data-ttu-id="d6eae-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d6eae-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="d6eae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6eae-102">SYNOPSIS</span></span>
<span data-ttu-id="d6eae-103">Beendet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="d6eae-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6eae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6eae-104">SYNTAX</span></span>

### <span data-ttu-id="d6eae-105">S1</span><span class="sxs-lookup"><span data-stu-id="d6eae-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6eae-106">S2</span><span class="sxs-lookup"><span data-stu-id="d6eae-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6eae-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6eae-107">DESCRIPTION</span></span>
<span data-ttu-id="d6eae-108">Das Cmdlet **Stop-AzureRmWebAppSlot** beendet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="d6eae-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="d6eae-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6eae-109">EXAMPLES</span></span>

### <span data-ttu-id="d6eae-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6eae-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="d6eae-111">Mit diesem Befehl wird der Slot Slot001 in Bezug auf die Web-App mit dem Namen ContosoWebApp, die zu der Ressourcengruppe Default-Web-westus gehört, beendet.</span><span class="sxs-lookup"><span data-stu-id="d6eae-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d6eae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6eae-112">PARAMETERS</span></span>

### <span data-ttu-id="d6eae-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d6eae-113">-Name</span></span>
<span data-ttu-id="d6eae-114">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="d6eae-114">WebApp Name</span></span>

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

### <span data-ttu-id="d6eae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6eae-115">-ResourceGroupName</span></span>
<span data-ttu-id="d6eae-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d6eae-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d6eae-117">-Slot</span><span class="sxs-lookup"><span data-stu-id="d6eae-117">-Slot</span></span>
<span data-ttu-id="d6eae-118">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="d6eae-118">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6eae-119">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="d6eae-119">-WebApp</span></span>
<span data-ttu-id="d6eae-120">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="d6eae-120">WebApp Object</span></span>

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

### <span data-ttu-id="d6eae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6eae-121">-DefaultProfile</span></span>
<span data-ttu-id="d6eae-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6eae-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6eae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6eae-123">CommonParameters</span></span>
<span data-ttu-id="d6eae-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6eae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6eae-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6eae-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6eae-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6eae-126">INPUTS</span></span>

### <span data-ttu-id="d6eae-127">Website</span><span class="sxs-lookup"><span data-stu-id="d6eae-127">Site</span></span>
<span data-ttu-id="d6eae-128">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6eae-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d6eae-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6eae-129">OUTPUTS</span></span>

## <span data-ttu-id="d6eae-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6eae-130">NOTES</span></span>

## <span data-ttu-id="d6eae-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6eae-131">RELATED LINKS</span></span>


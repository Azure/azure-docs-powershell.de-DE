---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 196e653447204b65c7f431e29fe76078a268dda1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664709"
---
# <span data-ttu-id="98f53-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="98f53-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="98f53-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98f53-102">SYNOPSIS</span></span>
<span data-ttu-id="98f53-103">Abrufen der Liste der config-Namen für Web App-Steckplätze</span><span class="sxs-lookup"><span data-stu-id="98f53-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98f53-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98f53-104">SYNTAX</span></span>

### <span data-ttu-id="98f53-105">S1</span><span class="sxs-lookup"><span data-stu-id="98f53-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98f53-106">S2</span><span class="sxs-lookup"><span data-stu-id="98f53-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98f53-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98f53-107">DESCRIPTION</span></span>
<span data-ttu-id="98f53-108">Das Cmdlet " **Get-AzureRmWebAppSlotConfigName** " Ruft die Liste der App-Einstellungen und Verbindungszeichenfolgen-Namen ab, die derzeit als sloteinstellungen markiert sind.</span><span class="sxs-lookup"><span data-stu-id="98f53-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="98f53-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98f53-109">EXAMPLES</span></span>

### <span data-ttu-id="98f53-110">1:</span><span class="sxs-lookup"><span data-stu-id="98f53-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="98f53-111">Dieser Befehl ruft App-Einstellungen und Verbindungszeichenfolgen in Bezug auf die Web-App mit dem Namen ContosoSite ab, die der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="98f53-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="98f53-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="98f53-112">PARAMETERS</span></span>

### <span data-ttu-id="98f53-113">-Name</span><span class="sxs-lookup"><span data-stu-id="98f53-113">-Name</span></span>
<span data-ttu-id="98f53-114">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="98f53-114">WebApp Name</span></span>

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

### <span data-ttu-id="98f53-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f53-115">-ResourceGroupName</span></span>
<span data-ttu-id="98f53-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="98f53-116">Resource Group Name</span></span>

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

### <span data-ttu-id="98f53-117">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="98f53-117">-WebApp</span></span>
<span data-ttu-id="98f53-118">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="98f53-118">WebApp Object</span></span>

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

### <span data-ttu-id="98f53-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f53-119">-DefaultProfile</span></span>
<span data-ttu-id="98f53-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="98f53-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98f53-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f53-121">CommonParameters</span></span>
<span data-ttu-id="98f53-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f53-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f53-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f53-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f53-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98f53-124">INPUTS</span></span>

### <span data-ttu-id="98f53-125">Website</span><span class="sxs-lookup"><span data-stu-id="98f53-125">Site</span></span>
<span data-ttu-id="98f53-126">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="98f53-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="98f53-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98f53-127">OUTPUTS</span></span>

## <span data-ttu-id="98f53-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="98f53-128">NOTES</span></span>

## <span data-ttu-id="98f53-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98f53-129">RELATED LINKS</span></span>


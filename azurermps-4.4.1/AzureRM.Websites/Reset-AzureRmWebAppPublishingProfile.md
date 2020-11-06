---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: f1224ae7ad95598d8ae947d0e38ef3a9cf7a4dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479834"
---
# <span data-ttu-id="6c412-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="6c412-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="6c412-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c412-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c412-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c412-103">SYNTAX</span></span>

### <span data-ttu-id="6c412-104">S1</span><span class="sxs-lookup"><span data-stu-id="6c412-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c412-105">S2</span><span class="sxs-lookup"><span data-stu-id="6c412-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c412-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c412-106">DESCRIPTION</span></span>
<span data-ttu-id="6c412-107">Das Cmdlet **Reset-AzureRmWebAppPublishingProfile** setzt das Veröffentlichungsprofil für die angegebene Web-App zurück.</span><span class="sxs-lookup"><span data-stu-id="6c412-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="6c412-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c412-108">EXAMPLES</span></span>

### <span data-ttu-id="6c412-109">1:</span><span class="sxs-lookup"><span data-stu-id="6c412-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="6c412-110">Mit diesem Befehl wird das Veröffentlichungsprofil für das Web-App-ContosoWebApp zurückgesetzt, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6c412-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6c412-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c412-111">PARAMETERS</span></span>

### <span data-ttu-id="6c412-112">-Name</span><span class="sxs-lookup"><span data-stu-id="6c412-112">-Name</span></span>
<span data-ttu-id="6c412-113">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="6c412-113">WebApp Name</span></span>

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

### <span data-ttu-id="6c412-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c412-114">-ResourceGroupName</span></span>
<span data-ttu-id="6c412-115">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="6c412-115">Resource Group Name</span></span>

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

### <span data-ttu-id="6c412-116">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="6c412-116">-WebApp</span></span>
<span data-ttu-id="6c412-117">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="6c412-117">WebApp Object</span></span>

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

### <span data-ttu-id="6c412-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c412-118">-DefaultProfile</span></span>
<span data-ttu-id="6c412-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c412-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c412-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c412-120">CommonParameters</span></span>
<span data-ttu-id="6c412-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c412-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c412-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c412-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c412-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c412-123">INPUTS</span></span>

### <span data-ttu-id="6c412-124">Website</span><span class="sxs-lookup"><span data-stu-id="6c412-124">Site</span></span>
<span data-ttu-id="6c412-125">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c412-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6c412-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c412-126">OUTPUTS</span></span>

## <span data-ttu-id="6c412-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c412-127">NOTES</span></span>

## <span data-ttu-id="6c412-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c412-128">RELATED LINKS</span></span>


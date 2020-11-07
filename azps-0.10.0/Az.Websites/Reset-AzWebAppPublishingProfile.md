---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 519a072a0c51f489a78992e483dec8aa9cd1fab5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842712"
---
# <span data-ttu-id="d9670-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="d9670-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="d9670-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9670-102">SYNOPSIS</span></span>

## <span data-ttu-id="d9670-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9670-103">SYNTAX</span></span>

### <span data-ttu-id="d9670-104">S1</span><span class="sxs-lookup"><span data-stu-id="d9670-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9670-105">S2</span><span class="sxs-lookup"><span data-stu-id="d9670-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9670-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9670-106">DESCRIPTION</span></span>
<span data-ttu-id="d9670-107">Das Cmdlet **Reset-AzWebAppPublishingProfile** setzt das Veröffentlichungsprofil für die angegebene Web-App zurück.</span><span class="sxs-lookup"><span data-stu-id="d9670-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="d9670-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9670-108">EXAMPLES</span></span>

### <span data-ttu-id="d9670-109">1:</span><span class="sxs-lookup"><span data-stu-id="d9670-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="d9670-110">Mit diesem Befehl wird das Veröffentlichungsprofil für das Web-App-ContosoWebApp zurückgesetzt, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d9670-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d9670-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9670-111">PARAMETERS</span></span>

### <span data-ttu-id="d9670-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9670-112">-DefaultProfile</span></span>
<span data-ttu-id="d9670-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9670-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9670-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d9670-114">-Name</span></span>
<span data-ttu-id="d9670-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="d9670-115">WebApp Name</span></span>

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

### <span data-ttu-id="d9670-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9670-116">-ResourceGroupName</span></span>
<span data-ttu-id="d9670-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d9670-117">Resource Group Name</span></span>

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

### <span data-ttu-id="d9670-118">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="d9670-118">-WebApp</span></span>
<span data-ttu-id="d9670-119">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="d9670-119">WebApp Object</span></span>

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

### <span data-ttu-id="d9670-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9670-120">CommonParameters</span></span>
<span data-ttu-id="d9670-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9670-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9670-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9670-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9670-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9670-123">INPUTS</span></span>

### <span data-ttu-id="d9670-124">Website</span><span class="sxs-lookup"><span data-stu-id="d9670-124">Site</span></span>
<span data-ttu-id="d9670-125">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d9670-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d9670-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9670-126">OUTPUTS</span></span>

## <span data-ttu-id="d9670-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9670-127">NOTES</span></span>

## <span data-ttu-id="d9670-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9670-128">RELATED LINKS</span></span>


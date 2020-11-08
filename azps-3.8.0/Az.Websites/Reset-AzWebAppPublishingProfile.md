---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 6a67fe30bfe6aaef21c094b126b9e1e3d92d468c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003123"
---
# <span data-ttu-id="d3f63-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="d3f63-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="d3f63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3f63-102">SYNOPSIS</span></span>

## <span data-ttu-id="d3f63-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3f63-103">SYNTAX</span></span>

### <span data-ttu-id="d3f63-104">S1</span><span class="sxs-lookup"><span data-stu-id="d3f63-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f63-105">S2</span><span class="sxs-lookup"><span data-stu-id="d3f63-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3f63-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3f63-106">DESCRIPTION</span></span>
<span data-ttu-id="d3f63-107">Das Cmdlet **Reset-AzWebAppPublishingProfile** setzt das Veröffentlichungsprofil für die angegebene Web-App zurück.</span><span class="sxs-lookup"><span data-stu-id="d3f63-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="d3f63-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3f63-108">EXAMPLES</span></span>

### <span data-ttu-id="d3f63-109">1:</span><span class="sxs-lookup"><span data-stu-id="d3f63-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="d3f63-110">Mit diesem Befehl wird das Veröffentlichungsprofil für das Web-App-ContosoWebApp zurückgesetzt, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3f63-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d3f63-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3f63-111">PARAMETERS</span></span>

### <span data-ttu-id="d3f63-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f63-112">-DefaultProfile</span></span>
<span data-ttu-id="d3f63-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3f63-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f63-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d3f63-114">-Name</span></span>
<span data-ttu-id="d3f63-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="d3f63-115">WebApp Name</span></span>

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

### <span data-ttu-id="d3f63-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f63-116">-ResourceGroupName</span></span>
<span data-ttu-id="d3f63-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d3f63-117">Resource Group Name</span></span>

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

### <span data-ttu-id="d3f63-118">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="d3f63-118">-WebApp</span></span>
<span data-ttu-id="d3f63-119">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="d3f63-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f63-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f63-120">CommonParameters</span></span>
<span data-ttu-id="d3f63-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f63-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f63-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f63-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f63-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3f63-123">INPUTS</span></span>

### <span data-ttu-id="d3f63-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f63-124">System.String</span></span>

### <span data-ttu-id="d3f63-125">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="d3f63-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d3f63-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3f63-126">OUTPUTS</span></span>

### <span data-ttu-id="d3f63-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f63-127">System.String</span></span>

## <span data-ttu-id="d3f63-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3f63-128">NOTES</span></span>

## <span data-ttu-id="d3f63-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3f63-129">RELATED LINKS</span></span>

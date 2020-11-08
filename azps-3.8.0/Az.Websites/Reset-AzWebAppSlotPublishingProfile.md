---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 8670581b376fe185ae4e477524f8f0a01c7cd3a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003122"
---
# <span data-ttu-id="23322-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="23322-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="23322-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23322-102">SYNOPSIS</span></span>

## <span data-ttu-id="23322-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="23322-103">SYNTAX</span></span>

### <span data-ttu-id="23322-104">S1</span><span class="sxs-lookup"><span data-stu-id="23322-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23322-105">S2</span><span class="sxs-lookup"><span data-stu-id="23322-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23322-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23322-106">DESCRIPTION</span></span>
<span data-ttu-id="23322-107">Das Cmdlet **Reset-AzWebAppSlotPublishingProfile** setzt das Veröffentlichungsprofil für den angegebenen Web App-Slot zurück.</span><span class="sxs-lookup"><span data-stu-id="23322-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="23322-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23322-108">EXAMPLES</span></span>

### <span data-ttu-id="23322-109">1:</span><span class="sxs-lookup"><span data-stu-id="23322-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="23322-110">Mit diesem Befehl wird das Veröffentlichungsprofil für den Steckplatz mit dem Namen slot001 für das Web-App-ContosoWebApp zurückgesetzt, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="23322-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="23322-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="23322-111">PARAMETERS</span></span>

### <span data-ttu-id="23322-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23322-112">-DefaultProfile</span></span>
<span data-ttu-id="23322-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23322-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23322-114">-Name</span><span class="sxs-lookup"><span data-stu-id="23322-114">-Name</span></span>
<span data-ttu-id="23322-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="23322-115">WebApp Name</span></span>

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

### <span data-ttu-id="23322-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23322-116">-ResourceGroupName</span></span>
<span data-ttu-id="23322-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="23322-117">Resource Group Name</span></span>

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

### <span data-ttu-id="23322-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="23322-118">-Slot</span></span>
<span data-ttu-id="23322-119">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="23322-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="23322-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="23322-120">-WebApp</span></span>
<span data-ttu-id="23322-121">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="23322-121">WebApp Object</span></span>

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

### <span data-ttu-id="23322-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23322-122">CommonParameters</span></span>
<span data-ttu-id="23322-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23322-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23322-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23322-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23322-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23322-125">INPUTS</span></span>

### <span data-ttu-id="23322-126">System. String</span><span class="sxs-lookup"><span data-stu-id="23322-126">System.String</span></span>

### <span data-ttu-id="23322-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="23322-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="23322-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23322-128">OUTPUTS</span></span>

### <span data-ttu-id="23322-129">System. String</span><span class="sxs-lookup"><span data-stu-id="23322-129">System.String</span></span>

## <span data-ttu-id="23322-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="23322-130">NOTES</span></span>

## <span data-ttu-id="23322-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23322-131">RELATED LINKS</span></span>

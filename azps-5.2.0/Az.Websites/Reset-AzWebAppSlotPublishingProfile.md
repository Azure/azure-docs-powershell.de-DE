---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291029"
---
# <span data-ttu-id="17dfb-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="17dfb-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="17dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17dfb-102">SYNOPSIS</span></span>

## <span data-ttu-id="17dfb-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17dfb-103">SYNTAX</span></span>

### <span data-ttu-id="17dfb-104">S1</span><span class="sxs-lookup"><span data-stu-id="17dfb-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17dfb-105">S2</span><span class="sxs-lookup"><span data-stu-id="17dfb-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17dfb-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17dfb-106">DESCRIPTION</span></span>
<span data-ttu-id="17dfb-107">Das **Cmdlet "Reset-AzWebAppSlotPublishingProfile"** setzt das Veröffentlichungsprofil für den angegebenen Web -App-Slot zurück.</span><span class="sxs-lookup"><span data-stu-id="17dfb-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="17dfb-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17dfb-108">EXAMPLES</span></span>

### <span data-ttu-id="17dfb-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17dfb-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="17dfb-110">Mit diesem Befehl wird das Veröffentlichungsprofil für das Slot "slot001" für die Web App "ContosoWebApp" zurückgesetzt, die der Ressourcengruppe "Default-Web-WestUS" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="17dfb-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="17dfb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17dfb-111">PARAMETERS</span></span>

### <span data-ttu-id="17dfb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17dfb-112">-DefaultProfile</span></span>
<span data-ttu-id="17dfb-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17dfb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17dfb-114">-Name</span><span class="sxs-lookup"><span data-stu-id="17dfb-114">-Name</span></span>
<span data-ttu-id="17dfb-115">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="17dfb-115">WebApp Name</span></span>

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

### <span data-ttu-id="17dfb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17dfb-116">-ResourceGroupName</span></span>
<span data-ttu-id="17dfb-117">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="17dfb-117">Resource Group Name</span></span>

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

### <span data-ttu-id="17dfb-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="17dfb-118">-Slot</span></span>
<span data-ttu-id="17dfb-119">Name des WebApp-Slot</span><span class="sxs-lookup"><span data-stu-id="17dfb-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="17dfb-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="17dfb-120">-WebApp</span></span>
<span data-ttu-id="17dfb-121">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="17dfb-121">WebApp Object</span></span>

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

### <span data-ttu-id="17dfb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17dfb-122">CommonParameters</span></span>
<span data-ttu-id="17dfb-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17dfb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17dfb-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17dfb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17dfb-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17dfb-125">INPUTS</span></span>

### <span data-ttu-id="17dfb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="17dfb-126">System.String</span></span>

### <span data-ttu-id="17dfb-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="17dfb-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="17dfb-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17dfb-128">OUTPUTS</span></span>

### <span data-ttu-id="17dfb-129">System.String</span><span class="sxs-lookup"><span data-stu-id="17dfb-129">System.String</span></span>

## <span data-ttu-id="17dfb-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="17dfb-130">NOTES</span></span>

## <span data-ttu-id="17dfb-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="17dfb-131">RELATED LINKS</span></span>

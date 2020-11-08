---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009500"
---
# <span data-ttu-id="7463e-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="7463e-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="7463e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7463e-102">SYNOPSIS</span></span>

## <span data-ttu-id="7463e-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="7463e-103">SYNTAX</span></span>

### <span data-ttu-id="7463e-104">S1</span><span class="sxs-lookup"><span data-stu-id="7463e-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7463e-105">S2</span><span class="sxs-lookup"><span data-stu-id="7463e-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7463e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7463e-106">DESCRIPTION</span></span>
<span data-ttu-id="7463e-107">Das Cmdlet **Reset-AzWebAppSlotPublishingProfile** setzt das Veröffentlichungsprofil für den angegebenen Web App-Slot zurück.</span><span class="sxs-lookup"><span data-stu-id="7463e-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="7463e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7463e-108">EXAMPLES</span></span>

### <span data-ttu-id="7463e-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7463e-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="7463e-110">Mit diesem Befehl wird das Veröffentlichungsprofil für den Steckplatz mit dem Namen slot001 für das Web-App-ContosoWebApp zurückgesetzt, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7463e-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="7463e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7463e-111">PARAMETERS</span></span>

### <span data-ttu-id="7463e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7463e-112">-DefaultProfile</span></span>
<span data-ttu-id="7463e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7463e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7463e-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7463e-114">-Name</span></span>
<span data-ttu-id="7463e-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="7463e-115">WebApp Name</span></span>

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

### <span data-ttu-id="7463e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7463e-116">-ResourceGroupName</span></span>
<span data-ttu-id="7463e-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7463e-117">Resource Group Name</span></span>

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

### <span data-ttu-id="7463e-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="7463e-118">-Slot</span></span>
<span data-ttu-id="7463e-119">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="7463e-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7463e-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="7463e-120">-WebApp</span></span>
<span data-ttu-id="7463e-121">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="7463e-121">WebApp Object</span></span>

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

### <span data-ttu-id="7463e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7463e-122">CommonParameters</span></span>
<span data-ttu-id="7463e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7463e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7463e-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7463e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7463e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7463e-125">INPUTS</span></span>

### <span data-ttu-id="7463e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7463e-126">System.String</span></span>

### <span data-ttu-id="7463e-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="7463e-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7463e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7463e-128">OUTPUTS</span></span>

### <span data-ttu-id="7463e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7463e-129">System.String</span></span>

## <span data-ttu-id="7463e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="7463e-130">NOTES</span></span>

## <span data-ttu-id="7463e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7463e-131">RELATED LINKS</span></span>

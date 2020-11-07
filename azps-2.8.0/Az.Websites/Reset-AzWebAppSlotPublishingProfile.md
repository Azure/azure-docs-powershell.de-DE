---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 0d67d2de8aebd251f4c02f19ff6a544325f2db5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826476"
---
# <span data-ttu-id="9e656-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="9e656-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="9e656-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e656-102">SYNOPSIS</span></span>

## <span data-ttu-id="9e656-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e656-103">SYNTAX</span></span>

### <span data-ttu-id="9e656-104">S1</span><span class="sxs-lookup"><span data-stu-id="9e656-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e656-105">S2</span><span class="sxs-lookup"><span data-stu-id="9e656-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e656-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e656-106">DESCRIPTION</span></span>
<span data-ttu-id="9e656-107">Das Cmdlet **Reset-AzWebAppSlotPublishingProfile** setzt das Veröffentlichungsprofil für den angegebenen Web App-Slot zurück.</span><span class="sxs-lookup"><span data-stu-id="9e656-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="9e656-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e656-108">EXAMPLES</span></span>

### <span data-ttu-id="9e656-109">1:</span><span class="sxs-lookup"><span data-stu-id="9e656-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="9e656-110">Mit diesem Befehl wird das Veröffentlichungsprofil für den Steckplatz mit dem Namen slot001 für das Web-App-ContosoWebApp zurückgesetzt, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9e656-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9e656-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e656-111">PARAMETERS</span></span>

### <span data-ttu-id="9e656-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e656-112">-DefaultProfile</span></span>
<span data-ttu-id="9e656-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e656-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e656-114">-Name</span><span class="sxs-lookup"><span data-stu-id="9e656-114">-Name</span></span>
<span data-ttu-id="9e656-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9e656-115">WebApp Name</span></span>

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

### <span data-ttu-id="9e656-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e656-116">-ResourceGroupName</span></span>
<span data-ttu-id="9e656-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9e656-117">Resource Group Name</span></span>

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

### <span data-ttu-id="9e656-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="9e656-118">-Slot</span></span>
<span data-ttu-id="9e656-119">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="9e656-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="9e656-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="9e656-120">-WebApp</span></span>
<span data-ttu-id="9e656-121">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="9e656-121">WebApp Object</span></span>

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

### <span data-ttu-id="9e656-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e656-122">CommonParameters</span></span>
<span data-ttu-id="9e656-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e656-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e656-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e656-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e656-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e656-125">INPUTS</span></span>

### <span data-ttu-id="9e656-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9e656-126">System.String</span></span>

### <span data-ttu-id="9e656-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9e656-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9e656-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e656-128">OUTPUTS</span></span>

### <span data-ttu-id="9e656-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9e656-129">System.String</span></span>

## <span data-ttu-id="9e656-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e656-130">NOTES</span></span>

## <span data-ttu-id="9e656-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e656-131">RELATED LINKS</span></span>

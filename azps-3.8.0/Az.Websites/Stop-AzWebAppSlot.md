---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: eba40b4c372fd900ac42bead0e2c0b39305c91cc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997286"
---
# <span data-ttu-id="8b307-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8b307-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="8b307-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b307-102">SYNOPSIS</span></span>
<span data-ttu-id="8b307-103">Beendet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="8b307-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="8b307-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b307-104">SYNTAX</span></span>

### <span data-ttu-id="8b307-105">S1</span><span class="sxs-lookup"><span data-stu-id="8b307-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b307-106">S2</span><span class="sxs-lookup"><span data-stu-id="8b307-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b307-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b307-107">DESCRIPTION</span></span>
<span data-ttu-id="8b307-108">Das Cmdlet **Stop-AzWebAppSlot** beendet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="8b307-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="8b307-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b307-109">EXAMPLES</span></span>

### <span data-ttu-id="8b307-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b307-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="8b307-111">Mit diesem Befehl wird der Slot Slot001 in Bezug auf die Web-App mit dem Namen ContosoWebApp, die zu der Ressourcengruppe Default-Web-westus gehört, beendet.</span><span class="sxs-lookup"><span data-stu-id="8b307-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8b307-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b307-112">PARAMETERS</span></span>

### <span data-ttu-id="8b307-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b307-113">-DefaultProfile</span></span>
<span data-ttu-id="8b307-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b307-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b307-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8b307-115">-Name</span></span>
<span data-ttu-id="8b307-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="8b307-116">WebApp Name</span></span>

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

### <span data-ttu-id="8b307-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b307-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b307-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8b307-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8b307-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="8b307-119">-Slot</span></span>
<span data-ttu-id="8b307-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="8b307-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8b307-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="8b307-121">-WebApp</span></span>
<span data-ttu-id="8b307-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="8b307-122">WebApp Object</span></span>

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

### <span data-ttu-id="8b307-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b307-123">CommonParameters</span></span>
<span data-ttu-id="8b307-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b307-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b307-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b307-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b307-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b307-126">INPUTS</span></span>

### <span data-ttu-id="8b307-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8b307-127">System.String</span></span>

### <span data-ttu-id="8b307-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8b307-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8b307-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b307-129">OUTPUTS</span></span>

### <span data-ttu-id="8b307-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8b307-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8b307-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b307-131">NOTES</span></span>

## <span data-ttu-id="8b307-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b307-132">RELATED LINKS</span></span>

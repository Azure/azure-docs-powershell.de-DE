---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: eba40b4c372fd900ac42bead0e2c0b39305c91cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164420"
---
# <span data-ttu-id="8a56d-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8a56d-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="8a56d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a56d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a56d-103">Beendet einen Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="8a56d-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="8a56d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a56d-104">SYNTAX</span></span>

### <span data-ttu-id="8a56d-105">S1</span><span class="sxs-lookup"><span data-stu-id="8a56d-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a56d-106">S2</span><span class="sxs-lookup"><span data-stu-id="8a56d-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a56d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a56d-107">DESCRIPTION</span></span>
<span data-ttu-id="8a56d-108">Das **Cmdlet "Stop-AzWebAppSlot"** beendet ein Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="8a56d-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="8a56d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a56d-109">EXAMPLES</span></span>

### <span data-ttu-id="8a56d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a56d-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="8a56d-111">Dieser Befehl stoppt den Slot Slot001, der sich auf die Web App namens "ContosoWebApp" bezieht, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="8a56d-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8a56d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a56d-112">PARAMETERS</span></span>

### <span data-ttu-id="8a56d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a56d-113">-DefaultProfile</span></span>
<span data-ttu-id="8a56d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a56d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a56d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8a56d-115">-Name</span></span>
<span data-ttu-id="8a56d-116">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="8a56d-116">WebApp Name</span></span>

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

### <span data-ttu-id="8a56d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a56d-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a56d-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8a56d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8a56d-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="8a56d-119">-Slot</span></span>
<span data-ttu-id="8a56d-120">Name des WebApp-Slot</span><span class="sxs-lookup"><span data-stu-id="8a56d-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8a56d-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8a56d-121">-WebApp</span></span>
<span data-ttu-id="8a56d-122">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="8a56d-122">WebApp Object</span></span>

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

### <span data-ttu-id="8a56d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a56d-123">CommonParameters</span></span>
<span data-ttu-id="8a56d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a56d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a56d-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a56d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a56d-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a56d-126">INPUTS</span></span>

### <span data-ttu-id="8a56d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8a56d-127">System.String</span></span>

### <span data-ttu-id="8a56d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8a56d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8a56d-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a56d-129">OUTPUTS</span></span>

### <span data-ttu-id="8a56d-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8a56d-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8a56d-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8a56d-131">NOTES</span></span>

## <span data-ttu-id="8a56d-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8a56d-132">RELATED LINKS</span></span>

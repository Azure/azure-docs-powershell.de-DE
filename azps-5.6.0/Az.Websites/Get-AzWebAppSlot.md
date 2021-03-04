---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 2f57ba64880f40a411ccac3263fa973815c685f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949851"
---
# <span data-ttu-id="58fc3-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="58fc3-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="58fc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="58fc3-103">Ruft einen Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="58fc3-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="58fc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58fc3-104">SYNTAX</span></span>

### <span data-ttu-id="58fc3-105">S1</span><span class="sxs-lookup"><span data-stu-id="58fc3-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58fc3-106">S2</span><span class="sxs-lookup"><span data-stu-id="58fc3-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58fc3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58fc3-107">DESCRIPTION</span></span>
<span data-ttu-id="58fc3-108">Das **Get-AzWebAppSlot-Cmdlet** ruft Informationen zu einem Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="58fc3-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="58fc3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58fc3-109">EXAMPLES</span></span>

### <span data-ttu-id="58fc3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58fc3-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="58fc3-111">Dieser Befehl ruft den Slot mit dem Namen Slot001 aus der Web App mit dem Namen WebAppStandard ab, die zur Ressourcengruppe Default-Web-WestUS gehört.</span><span class="sxs-lookup"><span data-stu-id="58fc3-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="58fc3-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="58fc3-112">PARAMETERS</span></span>

### <span data-ttu-id="58fc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58fc3-113">-DefaultProfile</span></span>
<span data-ttu-id="58fc3-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58fc3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58fc3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="58fc3-115">-Name</span></span>
<span data-ttu-id="58fc3-116">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="58fc3-116">WebApp Name</span></span>

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

### <span data-ttu-id="58fc3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58fc3-117">-ResourceGroupName</span></span>
<span data-ttu-id="58fc3-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="58fc3-118">Resource Group Name</span></span>

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

### <span data-ttu-id="58fc3-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="58fc3-119">-Slot</span></span>
<span data-ttu-id="58fc3-120">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="58fc3-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fc3-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="58fc3-121">-WebApp</span></span>
<span data-ttu-id="58fc3-122">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="58fc3-122">WebApp Object</span></span>

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

### <span data-ttu-id="58fc3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58fc3-123">CommonParameters</span></span>
<span data-ttu-id="58fc3-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58fc3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58fc3-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58fc3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58fc3-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58fc3-126">INPUTS</span></span>

### <span data-ttu-id="58fc3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="58fc3-127">System.String</span></span>

### <span data-ttu-id="58fc3-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="58fc3-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="58fc3-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58fc3-129">OUTPUTS</span></span>

### <span data-ttu-id="58fc3-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="58fc3-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="58fc3-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="58fc3-131">NOTES</span></span>

## <span data-ttu-id="58fc3-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="58fc3-132">RELATED LINKS</span></span>

[<span data-ttu-id="58fc3-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="58fc3-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="58fc3-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="58fc3-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="58fc3-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="58fc3-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="58fc3-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="58fc3-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="58fc3-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="58fc3-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="58fc3-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="58fc3-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="58fc3-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="58fc3-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

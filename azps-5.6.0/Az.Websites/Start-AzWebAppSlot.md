---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: c65eac94a9c44b3b7272116bc0e0757291b121b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948152"
---
# <span data-ttu-id="66ad4-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66ad4-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="66ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="66ad4-103">Startet einen Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="66ad4-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="66ad4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66ad4-104">SYNTAX</span></span>

### <span data-ttu-id="66ad4-105">S1</span><span class="sxs-lookup"><span data-stu-id="66ad4-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66ad4-106">S2</span><span class="sxs-lookup"><span data-stu-id="66ad4-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66ad4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66ad4-107">DESCRIPTION</span></span>
<span data-ttu-id="66ad4-108">Das **Cmdlet Start-AzWebAppSlot** startet einen Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="66ad4-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="66ad4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66ad4-109">EXAMPLES</span></span>

### <span data-ttu-id="66ad4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66ad4-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="66ad4-111">Mit diesem Befehl wird der Slot mit dem Namen Slot001 gestartet, der sich auf die Web App namens ContosoWebApp bezieht, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="66ad4-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="66ad4-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66ad4-112">PARAMETERS</span></span>

### <span data-ttu-id="66ad4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ad4-113">-DefaultProfile</span></span>
<span data-ttu-id="66ad4-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66ad4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66ad4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="66ad4-115">-Name</span></span>
<span data-ttu-id="66ad4-116">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="66ad4-116">WebApp Name</span></span>

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

### <span data-ttu-id="66ad4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66ad4-117">-ResourceGroupName</span></span>
<span data-ttu-id="66ad4-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="66ad4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="66ad4-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="66ad4-119">-Slot</span></span>
<span data-ttu-id="66ad4-120">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="66ad4-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="66ad4-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="66ad4-121">-WebApp</span></span>
<span data-ttu-id="66ad4-122">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="66ad4-122">WebApp Object</span></span>

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

### <span data-ttu-id="66ad4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ad4-123">CommonParameters</span></span>
<span data-ttu-id="66ad4-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66ad4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ad4-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66ad4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ad4-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66ad4-126">INPUTS</span></span>

### <span data-ttu-id="66ad4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="66ad4-127">System.String</span></span>

### <span data-ttu-id="66ad4-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="66ad4-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="66ad4-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66ad4-129">OUTPUTS</span></span>

### <span data-ttu-id="66ad4-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="66ad4-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="66ad4-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66ad4-131">NOTES</span></span>

## <span data-ttu-id="66ad4-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66ad4-132">RELATED LINKS</span></span>

[<span data-ttu-id="66ad4-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66ad4-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="66ad4-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66ad4-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="66ad4-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66ad4-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="66ad4-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66ad4-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="66ad4-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66ad4-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="66ad4-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="66ad4-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="66ad4-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="66ad4-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

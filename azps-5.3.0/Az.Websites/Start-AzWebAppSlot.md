---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460315"
---
# <span data-ttu-id="9891c-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9891c-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="9891c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9891c-102">SYNOPSIS</span></span>
<span data-ttu-id="9891c-103">Startet einen Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="9891c-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="9891c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9891c-104">SYNTAX</span></span>

### <span data-ttu-id="9891c-105">S1</span><span class="sxs-lookup"><span data-stu-id="9891c-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9891c-106">S2</span><span class="sxs-lookup"><span data-stu-id="9891c-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9891c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9891c-107">DESCRIPTION</span></span>
<span data-ttu-id="9891c-108">Das **Cmdlet "Start-AzWebAppSlot"** startet einen Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="9891c-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="9891c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9891c-109">EXAMPLES</span></span>

### <span data-ttu-id="9891c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9891c-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="9891c-111">Mit diesem Befehl wird das Slot "Slot001" gestartet, das sich auf die Web App namens "ContosoWebApp" bezieht, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="9891c-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="9891c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9891c-112">PARAMETERS</span></span>

### <span data-ttu-id="9891c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9891c-113">-DefaultProfile</span></span>
<span data-ttu-id="9891c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9891c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9891c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9891c-115">-Name</span></span>
<span data-ttu-id="9891c-116">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="9891c-116">WebApp Name</span></span>

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

### <span data-ttu-id="9891c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9891c-117">-ResourceGroupName</span></span>
<span data-ttu-id="9891c-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="9891c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="9891c-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="9891c-119">-Slot</span></span>
<span data-ttu-id="9891c-120">Name des WebApp-Slot</span><span class="sxs-lookup"><span data-stu-id="9891c-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="9891c-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9891c-121">-WebApp</span></span>
<span data-ttu-id="9891c-122">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="9891c-122">WebApp Object</span></span>

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

### <span data-ttu-id="9891c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9891c-123">CommonParameters</span></span>
<span data-ttu-id="9891c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9891c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9891c-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9891c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9891c-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9891c-126">INPUTS</span></span>

### <span data-ttu-id="9891c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9891c-127">System.String</span></span>

### <span data-ttu-id="9891c-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="9891c-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9891c-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9891c-129">OUTPUTS</span></span>

### <span data-ttu-id="9891c-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="9891c-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9891c-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9891c-131">NOTES</span></span>

## <span data-ttu-id="9891c-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9891c-132">RELATED LINKS</span></span>

[<span data-ttu-id="9891c-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9891c-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="9891c-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9891c-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="9891c-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9891c-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="9891c-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9891c-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="9891c-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9891c-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="9891c-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9891c-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="9891c-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9891c-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

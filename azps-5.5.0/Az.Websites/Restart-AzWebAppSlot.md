---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164465"
---
# <span data-ttu-id="41cb7-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41cb7-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="41cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41cb7-102">SYNOPSIS</span></span>

## <span data-ttu-id="41cb7-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41cb7-103">SYNTAX</span></span>

### <span data-ttu-id="41cb7-104">S1</span><span class="sxs-lookup"><span data-stu-id="41cb7-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41cb7-105">S2</span><span class="sxs-lookup"><span data-stu-id="41cb7-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41cb7-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41cb7-106">DESCRIPTION</span></span>
<span data-ttu-id="41cb7-107">Das **Cmdlet "Restart-AzWebAppSlot"** wird beendet und startet dann eine Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="41cb7-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="41cb7-108">Wenn sich das Web-App-Slot im angehaltenen Zustand befindet, verwenden Sie das Start-AzWebAppSlot Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41cb7-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="41cb7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="41cb7-109">EXAMPLES</span></span>

### <span data-ttu-id="41cb7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="41cb7-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="41cb7-111">Mit diesem Befehl wird der Slot Slot001 für die Web App ContosoWebApp neu gestartet, die der Ressourcengruppe "Default-Web-WestUS" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="41cb7-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="41cb7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41cb7-112">PARAMETERS</span></span>

### <span data-ttu-id="41cb7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cb7-113">-DefaultProfile</span></span>
<span data-ttu-id="41cb7-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41cb7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41cb7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="41cb7-115">-Name</span></span>
<span data-ttu-id="41cb7-116">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="41cb7-116">WebApp Name</span></span>

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

### <span data-ttu-id="41cb7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cb7-117">-ResourceGroupName</span></span>
<span data-ttu-id="41cb7-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="41cb7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="41cb7-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="41cb7-119">-Slot</span></span>
<span data-ttu-id="41cb7-120">Name des WebApp-Slot</span><span class="sxs-lookup"><span data-stu-id="41cb7-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="41cb7-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="41cb7-121">-WebApp</span></span>
<span data-ttu-id="41cb7-122">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="41cb7-122">WebApp Object</span></span>

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

### <span data-ttu-id="41cb7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cb7-123">CommonParameters</span></span>
<span data-ttu-id="41cb7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41cb7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cb7-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41cb7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cb7-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="41cb7-126">INPUTS</span></span>

### <span data-ttu-id="41cb7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="41cb7-127">System.String</span></span>

### <span data-ttu-id="41cb7-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="41cb7-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="41cb7-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="41cb7-129">OUTPUTS</span></span>

### <span data-ttu-id="41cb7-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="41cb7-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="41cb7-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="41cb7-131">NOTES</span></span>

## <span data-ttu-id="41cb7-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="41cb7-132">RELATED LINKS</span></span>

[<span data-ttu-id="41cb7-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41cb7-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="41cb7-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41cb7-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="41cb7-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41cb7-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="41cb7-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41cb7-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="41cb7-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41cb7-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="41cb7-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41cb7-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="41cb7-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="41cb7-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

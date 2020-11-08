---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997289"
---
# <span data-ttu-id="551bc-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="551bc-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="551bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="551bc-102">SYNOPSIS</span></span>
<span data-ttu-id="551bc-103">Startet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="551bc-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="551bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="551bc-104">SYNTAX</span></span>

### <span data-ttu-id="551bc-105">S1</span><span class="sxs-lookup"><span data-stu-id="551bc-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="551bc-106">S2</span><span class="sxs-lookup"><span data-stu-id="551bc-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="551bc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="551bc-107">DESCRIPTION</span></span>
<span data-ttu-id="551bc-108">Mit dem **Start-AzWebAppSlot-** Cmdlet wird ein Azure Web App-Steckplatz gestartet.</span><span class="sxs-lookup"><span data-stu-id="551bc-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="551bc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="551bc-109">EXAMPLES</span></span>

### <span data-ttu-id="551bc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="551bc-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="551bc-111">Mit diesem Befehl wird der Slot mit dem Namen Slot001 in Bezug auf die Web-App mit dem Namen ContosoWebApp gestartet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="551bc-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="551bc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="551bc-112">PARAMETERS</span></span>

### <span data-ttu-id="551bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551bc-113">-DefaultProfile</span></span>
<span data-ttu-id="551bc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="551bc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="551bc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="551bc-115">-Name</span></span>
<span data-ttu-id="551bc-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="551bc-116">WebApp Name</span></span>

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

### <span data-ttu-id="551bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="551bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="551bc-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="551bc-118">Resource Group Name</span></span>

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

### <span data-ttu-id="551bc-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="551bc-119">-Slot</span></span>
<span data-ttu-id="551bc-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="551bc-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="551bc-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="551bc-121">-WebApp</span></span>
<span data-ttu-id="551bc-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="551bc-122">WebApp Object</span></span>

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

### <span data-ttu-id="551bc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551bc-123">CommonParameters</span></span>
<span data-ttu-id="551bc-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551bc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551bc-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="551bc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551bc-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="551bc-126">INPUTS</span></span>

### <span data-ttu-id="551bc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="551bc-127">System.String</span></span>

### <span data-ttu-id="551bc-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="551bc-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="551bc-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="551bc-129">OUTPUTS</span></span>

### <span data-ttu-id="551bc-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="551bc-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="551bc-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="551bc-131">NOTES</span></span>

## <span data-ttu-id="551bc-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="551bc-132">RELATED LINKS</span></span>

[<span data-ttu-id="551bc-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="551bc-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="551bc-134">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="551bc-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="551bc-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="551bc-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="551bc-136">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="551bc-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="551bc-137">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="551bc-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="551bc-138">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="551bc-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="551bc-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="551bc-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

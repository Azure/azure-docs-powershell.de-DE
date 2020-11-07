---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 0535eee5dcdc3d0e78f95951fddcca9d7b8fff3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658492"
---
# <span data-ttu-id="3d963-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3d963-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="3d963-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d963-102">SYNOPSIS</span></span>
<span data-ttu-id="3d963-103">Startet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="3d963-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="3d963-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d963-104">SYNTAX</span></span>

### <span data-ttu-id="3d963-105">S1</span><span class="sxs-lookup"><span data-stu-id="3d963-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d963-106">S2</span><span class="sxs-lookup"><span data-stu-id="3d963-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d963-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d963-107">DESCRIPTION</span></span>
<span data-ttu-id="3d963-108">Mit dem **Start-AzWebAppSlot-** Cmdlet wird ein Azure Web App-Steckplatz gestartet.</span><span class="sxs-lookup"><span data-stu-id="3d963-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="3d963-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d963-109">EXAMPLES</span></span>

### <span data-ttu-id="3d963-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d963-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="3d963-111">Mit diesem Befehl wird der Slot mit dem Namen Slot001 in Bezug auf die Web-App mit dem Namen ContosoWebApp gestartet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="3d963-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3d963-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d963-112">PARAMETERS</span></span>

### <span data-ttu-id="3d963-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d963-113">-DefaultProfile</span></span>
<span data-ttu-id="3d963-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d963-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d963-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3d963-115">-Name</span></span>
<span data-ttu-id="3d963-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="3d963-116">WebApp Name</span></span>

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

### <span data-ttu-id="3d963-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d963-117">-ResourceGroupName</span></span>
<span data-ttu-id="3d963-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3d963-118">Resource Group Name</span></span>

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

### <span data-ttu-id="3d963-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="3d963-119">-Slot</span></span>
<span data-ttu-id="3d963-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="3d963-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="3d963-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="3d963-121">-WebApp</span></span>
<span data-ttu-id="3d963-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="3d963-122">WebApp Object</span></span>

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

### <span data-ttu-id="3d963-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d963-123">CommonParameters</span></span>
<span data-ttu-id="3d963-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d963-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d963-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d963-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d963-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d963-126">INPUTS</span></span>

### <span data-ttu-id="3d963-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3d963-127">System.String</span></span>

### <span data-ttu-id="3d963-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3d963-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3d963-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d963-129">OUTPUTS</span></span>

### <span data-ttu-id="3d963-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3d963-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3d963-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d963-131">NOTES</span></span>

## <span data-ttu-id="3d963-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d963-132">RELATED LINKS</span></span>

[<span data-ttu-id="3d963-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3d963-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="3d963-134">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3d963-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="3d963-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3d963-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="3d963-136">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3d963-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="3d963-137">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3d963-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="3d963-138">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3d963-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="3d963-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3d963-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

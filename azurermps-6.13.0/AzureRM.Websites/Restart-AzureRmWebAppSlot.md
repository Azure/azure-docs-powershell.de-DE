---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: 2d1c4fe635e6d4bc509f82f1af376ee0f662217a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497170"
---
# <span data-ttu-id="b1f44-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b1f44-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="b1f44-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1f44-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1f44-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1f44-103">SYNTAX</span></span>

### <span data-ttu-id="b1f44-104">S1</span><span class="sxs-lookup"><span data-stu-id="b1f44-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1f44-105">S2</span><span class="sxs-lookup"><span data-stu-id="b1f44-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1f44-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1f44-106">DESCRIPTION</span></span>
<span data-ttu-id="b1f44-107">Das Cmdlet " **Restart-AzureRmWebAppSlot** " beendet den Azure Web App-Slot und startet dann.</span><span class="sxs-lookup"><span data-stu-id="b1f44-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="b1f44-108">Wenn sich der Web App-Slot im Zustand "beendet" befindet, verwenden Sie das Cmdlet "Start-AzureRmWebAppSlot".</span><span class="sxs-lookup"><span data-stu-id="b1f44-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="b1f44-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1f44-109">EXAMPLES</span></span>

### <span data-ttu-id="b1f44-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1f44-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="b1f44-111">Mit diesem Befehl wird der Slot Slot001 für das Web-App-ContosoWebApp neu gestartet, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b1f44-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="b1f44-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1f44-112">PARAMETERS</span></span>

### <span data-ttu-id="b1f44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f44-113">-DefaultProfile</span></span>
<span data-ttu-id="b1f44-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1f44-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f44-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b1f44-115">-Name</span></span>
<span data-ttu-id="b1f44-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="b1f44-116">WebApp Name</span></span>

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

### <span data-ttu-id="b1f44-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f44-117">-ResourceGroupName</span></span>
<span data-ttu-id="b1f44-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b1f44-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b1f44-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="b1f44-119">-Slot</span></span>
<span data-ttu-id="b1f44-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="b1f44-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b1f44-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="b1f44-121">-WebApp</span></span>
<span data-ttu-id="b1f44-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="b1f44-122">WebApp Object</span></span>

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

### <span data-ttu-id="b1f44-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f44-123">CommonParameters</span></span>
<span data-ttu-id="b1f44-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f44-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f44-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1f44-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f44-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1f44-126">INPUTS</span></span>

### <span data-ttu-id="b1f44-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b1f44-127">System.String</span></span>

### <span data-ttu-id="b1f44-128">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="b1f44-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="b1f44-129">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="b1f44-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="b1f44-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1f44-130">OUTPUTS</span></span>

### <span data-ttu-id="b1f44-131">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="b1f44-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="b1f44-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1f44-132">NOTES</span></span>

## <span data-ttu-id="b1f44-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1f44-133">RELATED LINKS</span></span>

[<span data-ttu-id="b1f44-134">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b1f44-134">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="b1f44-135">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b1f44-135">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="b1f44-136">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b1f44-136">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="b1f44-137">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b1f44-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="b1f44-138">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b1f44-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="b1f44-139">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b1f44-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="b1f44-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b1f44-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

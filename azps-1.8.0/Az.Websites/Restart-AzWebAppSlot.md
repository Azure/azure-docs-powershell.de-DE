---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 53323aaf29145f4340dd00fa752d8afd2dd72131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658512"
---
# <span data-ttu-id="8d016-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d016-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="8d016-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d016-102">SYNOPSIS</span></span>

## <span data-ttu-id="8d016-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d016-103">SYNTAX</span></span>

### <span data-ttu-id="8d016-104">S1</span><span class="sxs-lookup"><span data-stu-id="8d016-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d016-105">S2</span><span class="sxs-lookup"><span data-stu-id="8d016-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d016-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d016-106">DESCRIPTION</span></span>
<span data-ttu-id="8d016-107">Das Cmdlet " **Restart-AzWebAppSlot** " beendet den Azure Web App-Slot und startet dann.</span><span class="sxs-lookup"><span data-stu-id="8d016-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="8d016-108">Wenn sich der Web App-Slot im Zustand "beendet" befindet, verwenden Sie das Cmdlet "Start-AzWebAppSlot".</span><span class="sxs-lookup"><span data-stu-id="8d016-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="8d016-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d016-109">EXAMPLES</span></span>

### <span data-ttu-id="8d016-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8d016-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="8d016-111">Mit diesem Befehl wird der Slot Slot001 für das Web-App-ContosoWebApp neu gestartet, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8d016-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="8d016-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d016-112">PARAMETERS</span></span>

### <span data-ttu-id="8d016-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d016-113">-DefaultProfile</span></span>
<span data-ttu-id="8d016-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d016-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d016-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8d016-115">-Name</span></span>
<span data-ttu-id="8d016-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="8d016-116">WebApp Name</span></span>

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

### <span data-ttu-id="8d016-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d016-117">-ResourceGroupName</span></span>
<span data-ttu-id="8d016-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8d016-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8d016-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="8d016-119">-Slot</span></span>
<span data-ttu-id="8d016-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="8d016-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8d016-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="8d016-121">-WebApp</span></span>
<span data-ttu-id="8d016-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="8d016-122">WebApp Object</span></span>

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

### <span data-ttu-id="8d016-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d016-123">CommonParameters</span></span>
<span data-ttu-id="8d016-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d016-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d016-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d016-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d016-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d016-126">INPUTS</span></span>

### <span data-ttu-id="8d016-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8d016-127">System.String</span></span>

### <span data-ttu-id="8d016-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8d016-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8d016-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d016-129">OUTPUTS</span></span>

### <span data-ttu-id="8d016-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="8d016-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8d016-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d016-131">NOTES</span></span>

## <span data-ttu-id="8d016-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d016-132">RELATED LINKS</span></span>

[<span data-ttu-id="8d016-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d016-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8d016-134">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d016-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="8d016-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d016-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8d016-136">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d016-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="8d016-137">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d016-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="8d016-138">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8d016-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8d016-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8d016-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003120"
---
# <span data-ttu-id="e5ddd-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e5ddd-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="e5ddd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ddd-103">Startet eine Azure Web App neu.</span><span class="sxs-lookup"><span data-stu-id="e5ddd-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="e5ddd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5ddd-104">SYNTAX</span></span>

### <span data-ttu-id="e5ddd-105">S1</span><span class="sxs-lookup"><span data-stu-id="e5ddd-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ddd-106">S2</span><span class="sxs-lookup"><span data-stu-id="e5ddd-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5ddd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5ddd-107">DESCRIPTION</span></span>
<span data-ttu-id="e5ddd-108">Das Cmdlet " **Restart-AzWebApp** " beendet und startet dann eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e5ddd-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="e5ddd-109">Wenn sich die Web-App im Zustand "beendet" befindet, verwenden Sie das Cmdlet "Start-AzWebApp".</span><span class="sxs-lookup"><span data-stu-id="e5ddd-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="e5ddd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5ddd-110">EXAMPLES</span></span>

### <span data-ttu-id="e5ddd-111">Beispiel 1: Erneutes Starten einer Web-App</span><span class="sxs-lookup"><span data-stu-id="e5ddd-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e5ddd-112">Mit diesem Befehl wird die Azure Web App mit dem Namen ContosoSite beendet, die zu der Ressourcengruppe Default-Web-westus gehört und dann neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e5ddd-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="e5ddd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5ddd-113">PARAMETERS</span></span>

### <span data-ttu-id="e5ddd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ddd-114">-DefaultProfile</span></span>
<span data-ttu-id="e5ddd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5ddd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5ddd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e5ddd-116">-Name</span></span>
<span data-ttu-id="e5ddd-117">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="e5ddd-117">WebApp Name</span></span>

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

### <span data-ttu-id="e5ddd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5ddd-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5ddd-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e5ddd-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e5ddd-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="e5ddd-120">-WebApp</span></span>
<span data-ttu-id="e5ddd-121">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="e5ddd-121">WebApp Object</span></span>

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

### <span data-ttu-id="e5ddd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ddd-122">CommonParameters</span></span>
<span data-ttu-id="e5ddd-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5ddd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ddd-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5ddd-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ddd-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5ddd-125">INPUTS</span></span>

### <span data-ttu-id="e5ddd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e5ddd-126">System.String</span></span>

### <span data-ttu-id="e5ddd-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e5ddd-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e5ddd-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5ddd-128">OUTPUTS</span></span>

### <span data-ttu-id="e5ddd-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e5ddd-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e5ddd-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5ddd-130">NOTES</span></span>

## <span data-ttu-id="e5ddd-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5ddd-131">RELATED LINKS</span></span>

[<span data-ttu-id="e5ddd-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e5ddd-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e5ddd-133">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e5ddd-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e5ddd-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e5ddd-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e5ddd-135">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e5ddd-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="e5ddd-136">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e5ddd-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



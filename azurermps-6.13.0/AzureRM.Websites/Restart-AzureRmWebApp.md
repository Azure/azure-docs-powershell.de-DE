---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: 42b561707dd1b4240cf0542adfb196250aafc8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497166"
---
# <span data-ttu-id="7d1a2-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1a2-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="7d1a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1a2-103">Startet eine Azure Web App neu.</span><span class="sxs-lookup"><span data-stu-id="7d1a2-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d1a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d1a2-104">SYNTAX</span></span>

### <span data-ttu-id="7d1a2-105">S1</span><span class="sxs-lookup"><span data-stu-id="7d1a2-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d1a2-106">S2</span><span class="sxs-lookup"><span data-stu-id="7d1a2-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d1a2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d1a2-107">DESCRIPTION</span></span>
<span data-ttu-id="7d1a2-108">Das Cmdlet " **Restart-AzureRmWebApp** " beendet und startet dann eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7d1a2-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="7d1a2-109">Wenn sich die Web-App im Zustand "beendet" befindet, verwenden Sie das Cmdlet "Start-AzureRmWebApp".</span><span class="sxs-lookup"><span data-stu-id="7d1a2-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="7d1a2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d1a2-110">EXAMPLES</span></span>

### <span data-ttu-id="7d1a2-111">Beispiel 1: Erneutes Starten einer Web-App</span><span class="sxs-lookup"><span data-stu-id="7d1a2-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="7d1a2-112">Mit diesem Befehl wird die Azure Web App mit dem Namen ContosoSite beendet, die zu der Ressourcengruppe Default-Web-westus gehört und dann neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7d1a2-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="7d1a2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d1a2-113">PARAMETERS</span></span>

### <span data-ttu-id="7d1a2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1a2-114">-DefaultProfile</span></span>
<span data-ttu-id="7d1a2-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d1a2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d1a2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7d1a2-116">-Name</span></span>
<span data-ttu-id="7d1a2-117">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="7d1a2-117">WebApp Name</span></span>

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

### <span data-ttu-id="7d1a2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1a2-118">-ResourceGroupName</span></span>
<span data-ttu-id="7d1a2-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7d1a2-119">Resource Group Name</span></span>

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

### <span data-ttu-id="7d1a2-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="7d1a2-120">-WebApp</span></span>
<span data-ttu-id="7d1a2-121">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="7d1a2-121">WebApp Object</span></span>

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

### <span data-ttu-id="7d1a2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1a2-122">CommonParameters</span></span>
<span data-ttu-id="7d1a2-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d1a2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1a2-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d1a2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1a2-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d1a2-125">INPUTS</span></span>

### <span data-ttu-id="7d1a2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7d1a2-126">System.String</span></span>

### <span data-ttu-id="7d1a2-127">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="7d1a2-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="7d1a2-128">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="7d1a2-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="7d1a2-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d1a2-129">OUTPUTS</span></span>

### <span data-ttu-id="7d1a2-130">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="7d1a2-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="7d1a2-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d1a2-131">NOTES</span></span>

## <span data-ttu-id="7d1a2-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d1a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="7d1a2-133">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1a2-133">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="7d1a2-134">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1a2-134">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="7d1a2-135">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1a2-135">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="7d1a2-136">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1a2-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="7d1a2-137">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d1a2-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)



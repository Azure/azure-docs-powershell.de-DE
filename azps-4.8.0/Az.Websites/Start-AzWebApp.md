---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166710"
---
# <span data-ttu-id="18a46-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="18a46-101">Start-AzWebApp</span></span>

## <span data-ttu-id="18a46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18a46-102">SYNOPSIS</span></span>
<span data-ttu-id="18a46-103">Startet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="18a46-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="18a46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18a46-104">SYNTAX</span></span>

### <span data-ttu-id="18a46-105">S1</span><span class="sxs-lookup"><span data-stu-id="18a46-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18a46-106">S2</span><span class="sxs-lookup"><span data-stu-id="18a46-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18a46-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18a46-107">DESCRIPTION</span></span>
<span data-ttu-id="18a46-108">Das Cmdlet **Start-AzWebApp** startet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="18a46-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="18a46-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18a46-109">EXAMPLES</span></span>

### <span data-ttu-id="18a46-110">Beispiel 1: Starten einer Web-App</span><span class="sxs-lookup"><span data-stu-id="18a46-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="18a46-111">Mit diesem Befehl wird die Web-App mit dem Namen ContosoWebApp gestartet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="18a46-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="18a46-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="18a46-112">PARAMETERS</span></span>

### <span data-ttu-id="18a46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a46-113">-DefaultProfile</span></span>
<span data-ttu-id="18a46-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18a46-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18a46-115">-Name</span><span class="sxs-lookup"><span data-stu-id="18a46-115">-Name</span></span>
<span data-ttu-id="18a46-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="18a46-116">WebApp Name</span></span>

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

### <span data-ttu-id="18a46-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a46-117">-ResourceGroupName</span></span>
<span data-ttu-id="18a46-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="18a46-118">Resource Group Name</span></span>

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

### <span data-ttu-id="18a46-119">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="18a46-119">-WebApp</span></span>
<span data-ttu-id="18a46-120">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="18a46-120">WebApp Object</span></span>

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

### <span data-ttu-id="18a46-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a46-121">CommonParameters</span></span>
<span data-ttu-id="18a46-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a46-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a46-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18a46-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a46-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18a46-124">INPUTS</span></span>

### <span data-ttu-id="18a46-125">System. String</span><span class="sxs-lookup"><span data-stu-id="18a46-125">System.String</span></span>

### <span data-ttu-id="18a46-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="18a46-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="18a46-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18a46-127">OUTPUTS</span></span>

### <span data-ttu-id="18a46-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="18a46-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="18a46-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="18a46-129">NOTES</span></span>

## <span data-ttu-id="18a46-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18a46-130">RELATED LINKS</span></span>

[<span data-ttu-id="18a46-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="18a46-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="18a46-132">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="18a46-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="18a46-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="18a46-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="18a46-134">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="18a46-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="18a46-135">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="18a46-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



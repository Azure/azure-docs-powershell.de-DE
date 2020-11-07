---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 09c618e617775e0c2bfffab1794f2427f97d811c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827263"
---
# <span data-ttu-id="f5f24-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5f24-101">Start-AzWebApp</span></span>

## <span data-ttu-id="f5f24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5f24-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f24-103">Startet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f5f24-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="f5f24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5f24-104">SYNTAX</span></span>

### <span data-ttu-id="f5f24-105">S1</span><span class="sxs-lookup"><span data-stu-id="f5f24-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5f24-106">S2</span><span class="sxs-lookup"><span data-stu-id="f5f24-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5f24-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5f24-107">DESCRIPTION</span></span>
<span data-ttu-id="f5f24-108">Das Cmdlet **Start-AzWebApp** startet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f5f24-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="f5f24-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5f24-109">EXAMPLES</span></span>

### <span data-ttu-id="f5f24-110">Beispiel 1: Starten einer Web-App</span><span class="sxs-lookup"><span data-stu-id="f5f24-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="f5f24-111">Mit diesem Befehl wird die Web-App mit dem Namen ContosoWebApp gestartet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="f5f24-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f5f24-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5f24-112">PARAMETERS</span></span>

### <span data-ttu-id="f5f24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f24-113">-DefaultProfile</span></span>
<span data-ttu-id="f5f24-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5f24-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5f24-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f5f24-115">-Name</span></span>
<span data-ttu-id="f5f24-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="f5f24-116">WebApp Name</span></span>

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

### <span data-ttu-id="f5f24-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f24-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5f24-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f5f24-118">Resource Group Name</span></span>

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

### <span data-ttu-id="f5f24-119">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="f5f24-119">-WebApp</span></span>
<span data-ttu-id="f5f24-120">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="f5f24-120">WebApp Object</span></span>

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

### <span data-ttu-id="f5f24-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f24-121">CommonParameters</span></span>
<span data-ttu-id="f5f24-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f24-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f24-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f24-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f24-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5f24-124">INPUTS</span></span>

### <span data-ttu-id="f5f24-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f5f24-125">System.String</span></span>

### <span data-ttu-id="f5f24-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f5f24-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f5f24-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5f24-127">OUTPUTS</span></span>

### <span data-ttu-id="f5f24-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f5f24-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f5f24-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5f24-129">NOTES</span></span>

## <span data-ttu-id="f5f24-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5f24-130">RELATED LINKS</span></span>

[<span data-ttu-id="f5f24-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5f24-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="f5f24-132">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5f24-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="f5f24-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5f24-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="f5f24-134">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5f24-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="f5f24-135">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5f24-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



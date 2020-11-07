---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: d533a2d7401236e374ca6f541e646cb85a080f9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842671"
---
# <span data-ttu-id="49c34-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49c34-101">Start-AzWebApp</span></span>

## <span data-ttu-id="49c34-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49c34-102">SYNOPSIS</span></span>
<span data-ttu-id="49c34-103">Startet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="49c34-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="49c34-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49c34-104">SYNTAX</span></span>

### <span data-ttu-id="49c34-105">S1</span><span class="sxs-lookup"><span data-stu-id="49c34-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49c34-106">S2</span><span class="sxs-lookup"><span data-stu-id="49c34-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49c34-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49c34-107">DESCRIPTION</span></span>
<span data-ttu-id="49c34-108">Das Cmdlet **Start-AzWebApp** startet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="49c34-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="49c34-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49c34-109">EXAMPLES</span></span>

### <span data-ttu-id="49c34-110">Beispiel 1: Starten einer Web-App</span><span class="sxs-lookup"><span data-stu-id="49c34-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="49c34-111">Mit diesem Befehl wird die Web-App mit dem Namen ContosoWebApp gestartet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="49c34-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="49c34-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="49c34-112">PARAMETERS</span></span>

### <span data-ttu-id="49c34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c34-113">-DefaultProfile</span></span>
<span data-ttu-id="49c34-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49c34-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c34-115">-Name</span><span class="sxs-lookup"><span data-stu-id="49c34-115">-Name</span></span>
<span data-ttu-id="49c34-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="49c34-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49c34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c34-117">-ResourceGroupName</span></span>
<span data-ttu-id="49c34-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="49c34-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49c34-119">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="49c34-119">-WebApp</span></span>
<span data-ttu-id="49c34-120">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="49c34-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49c34-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c34-121">CommonParameters</span></span>
<span data-ttu-id="49c34-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c34-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c34-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49c34-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c34-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49c34-124">INPUTS</span></span>

### <span data-ttu-id="49c34-125">Website</span><span class="sxs-lookup"><span data-stu-id="49c34-125">Site</span></span>
<span data-ttu-id="49c34-126">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="49c34-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="49c34-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49c34-127">OUTPUTS</span></span>

## <span data-ttu-id="49c34-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="49c34-128">NOTES</span></span>

## <span data-ttu-id="49c34-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49c34-129">RELATED LINKS</span></span>

[<span data-ttu-id="49c34-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49c34-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="49c34-131">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49c34-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="49c34-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49c34-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="49c34-133">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49c34-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="49c34-134">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="49c34-134">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



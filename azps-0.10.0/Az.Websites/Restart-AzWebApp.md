---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: 975b49af1e20c5b9f4839a561494eaeb8275f02f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842688"
---
# <span data-ttu-id="f589d-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f589d-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="f589d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f589d-102">SYNOPSIS</span></span>
<span data-ttu-id="f589d-103">Startet eine Azure Web App neu.</span><span class="sxs-lookup"><span data-stu-id="f589d-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="f589d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f589d-104">SYNTAX</span></span>

### <span data-ttu-id="f589d-105">S1</span><span class="sxs-lookup"><span data-stu-id="f589d-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f589d-106">S2</span><span class="sxs-lookup"><span data-stu-id="f589d-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f589d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f589d-107">DESCRIPTION</span></span>
<span data-ttu-id="f589d-108">Das Cmdlet " **Restart-AzWebApp** " beendet und startet dann eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f589d-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="f589d-109">Wenn sich die Web-App im Zustand "beendet" befindet, verwenden Sie das Cmdlet "Start-AzWebApp".</span><span class="sxs-lookup"><span data-stu-id="f589d-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="f589d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f589d-110">EXAMPLES</span></span>

### <span data-ttu-id="f589d-111">Beispiel 1: Erneutes Starten einer Web-App</span><span class="sxs-lookup"><span data-stu-id="f589d-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f589d-112">Mit diesem Befehl wird die Azure Web App mit dem Namen ContosoSite beendet, die zu der Ressourcengruppe Default-Web-westus gehört und dann neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f589d-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="f589d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f589d-113">PARAMETERS</span></span>

### <span data-ttu-id="f589d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f589d-114">-DefaultProfile</span></span>
<span data-ttu-id="f589d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f589d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f589d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f589d-116">-Name</span></span>
<span data-ttu-id="f589d-117">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="f589d-117">WebApp Name</span></span>

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

### <span data-ttu-id="f589d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f589d-118">-ResourceGroupName</span></span>
<span data-ttu-id="f589d-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f589d-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f589d-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="f589d-120">-WebApp</span></span>
<span data-ttu-id="f589d-121">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="f589d-121">WebApp Object</span></span>

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

### <span data-ttu-id="f589d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f589d-122">CommonParameters</span></span>
<span data-ttu-id="f589d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f589d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f589d-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f589d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f589d-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f589d-125">INPUTS</span></span>

### <span data-ttu-id="f589d-126">Website</span><span class="sxs-lookup"><span data-stu-id="f589d-126">Site</span></span>
<span data-ttu-id="f589d-127">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f589d-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f589d-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f589d-128">OUTPUTS</span></span>

## <span data-ttu-id="f589d-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f589d-129">NOTES</span></span>

## <span data-ttu-id="f589d-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f589d-130">RELATED LINKS</span></span>

[<span data-ttu-id="f589d-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f589d-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="f589d-132">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f589d-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="f589d-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f589d-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="f589d-134">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f589d-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="f589d-135">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f589d-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



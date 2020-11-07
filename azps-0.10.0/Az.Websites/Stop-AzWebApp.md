---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 073c98abe9db8b8a8d52c6d9bb06e64b028d379b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842643"
---
# <span data-ttu-id="538a7-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="538a7-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="538a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="538a7-102">SYNOPSIS</span></span>
<span data-ttu-id="538a7-103">Beendet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="538a7-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="538a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="538a7-104">SYNTAX</span></span>

### <span data-ttu-id="538a7-105">S1</span><span class="sxs-lookup"><span data-stu-id="538a7-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="538a7-106">S2</span><span class="sxs-lookup"><span data-stu-id="538a7-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="538a7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="538a7-107">DESCRIPTION</span></span>
<span data-ttu-id="538a7-108">Das Cmdlet **Stop-AzWebApp** beendet eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="538a7-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="538a7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="538a7-109">EXAMPLES</span></span>

### <span data-ttu-id="538a7-110">Beispiel 1: Beenden einer Web-App</span><span class="sxs-lookup"><span data-stu-id="538a7-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="538a7-111">Mit diesem Befehl wird die Web-App mit dem Namen ContosoWebApp beendet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="538a7-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="538a7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="538a7-112">PARAMETERS</span></span>

### <span data-ttu-id="538a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="538a7-113">-DefaultProfile</span></span>
<span data-ttu-id="538a7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="538a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="538a7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="538a7-115">-Name</span></span>
<span data-ttu-id="538a7-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="538a7-116">WebApp Name</span></span>

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

### <span data-ttu-id="538a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="538a7-117">-ResourceGroupName</span></span>
<span data-ttu-id="538a7-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="538a7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="538a7-119">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="538a7-119">-WebApp</span></span>
<span data-ttu-id="538a7-120">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="538a7-120">WebApp Object</span></span>

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

### <span data-ttu-id="538a7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="538a7-121">CommonParameters</span></span>
<span data-ttu-id="538a7-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="538a7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="538a7-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="538a7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="538a7-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="538a7-124">INPUTS</span></span>

### <span data-ttu-id="538a7-125">Website</span><span class="sxs-lookup"><span data-stu-id="538a7-125">Site</span></span>
<span data-ttu-id="538a7-126">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="538a7-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="538a7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="538a7-127">OUTPUTS</span></span>

## <span data-ttu-id="538a7-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="538a7-128">NOTES</span></span>

## <span data-ttu-id="538a7-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="538a7-129">RELATED LINKS</span></span>

[<span data-ttu-id="538a7-130">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="538a7-130">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="538a7-131">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="538a7-131">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="538a7-132">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="538a7-132">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="538a7-133">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="538a7-133">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="538a7-134">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="538a7-134">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



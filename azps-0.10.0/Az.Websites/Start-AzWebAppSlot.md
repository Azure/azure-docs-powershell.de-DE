---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: d843cf5eed70e230f81c704e9168fee917a77077
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842672"
---
# <span data-ttu-id="21cf9-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21cf9-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="21cf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="21cf9-103">Startet einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="21cf9-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="21cf9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21cf9-104">SYNTAX</span></span>

### <span data-ttu-id="21cf9-105">S1</span><span class="sxs-lookup"><span data-stu-id="21cf9-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21cf9-106">S2</span><span class="sxs-lookup"><span data-stu-id="21cf9-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21cf9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21cf9-107">DESCRIPTION</span></span>
<span data-ttu-id="21cf9-108">Mit dem **Start-AzWebAppSlot-** Cmdlet wird ein Azure Web App-Steckplatz gestartet.</span><span class="sxs-lookup"><span data-stu-id="21cf9-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="21cf9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21cf9-109">EXAMPLES</span></span>

### <span data-ttu-id="21cf9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="21cf9-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="21cf9-111">Mit diesem Befehl wird der Slot mit dem Namen Slot001 in Bezug auf die Web-App mit dem Namen ContosoWebApp gestartet, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="21cf9-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="21cf9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="21cf9-112">PARAMETERS</span></span>

### <span data-ttu-id="21cf9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21cf9-113">-DefaultProfile</span></span>
<span data-ttu-id="21cf9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21cf9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21cf9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="21cf9-115">-Name</span></span>
<span data-ttu-id="21cf9-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="21cf9-116">WebApp Name</span></span>

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

### <span data-ttu-id="21cf9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21cf9-117">-ResourceGroupName</span></span>
<span data-ttu-id="21cf9-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="21cf9-118">Resource Group Name</span></span>

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

### <span data-ttu-id="21cf9-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="21cf9-119">-Slot</span></span>
<span data-ttu-id="21cf9-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="21cf9-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21cf9-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="21cf9-121">-WebApp</span></span>
<span data-ttu-id="21cf9-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="21cf9-122">WebApp Object</span></span>

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

### <span data-ttu-id="21cf9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21cf9-123">CommonParameters</span></span>
<span data-ttu-id="21cf9-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21cf9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21cf9-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21cf9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21cf9-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21cf9-126">INPUTS</span></span>

### <span data-ttu-id="21cf9-127">Website</span><span class="sxs-lookup"><span data-stu-id="21cf9-127">Site</span></span>
<span data-ttu-id="21cf9-128">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="21cf9-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="21cf9-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21cf9-129">OUTPUTS</span></span>

## <span data-ttu-id="21cf9-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="21cf9-130">NOTES</span></span>

## <span data-ttu-id="21cf9-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21cf9-131">RELATED LINKS</span></span>

[<span data-ttu-id="21cf9-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21cf9-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="21cf9-133">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21cf9-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="21cf9-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21cf9-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="21cf9-135">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21cf9-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="21cf9-136">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21cf9-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="21cf9-137">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="21cf9-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="21cf9-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="21cf9-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

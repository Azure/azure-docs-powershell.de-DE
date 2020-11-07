---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 033b0bd4458f20153ec1e9c876f12c7e7c368c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842760"
---
# <span data-ttu-id="dc8b1-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc8b1-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="dc8b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8b1-103">Ruft einen Azure Web App-Steckplatz ab.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="dc8b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc8b1-104">SYNTAX</span></span>

### <span data-ttu-id="dc8b1-105">S1</span><span class="sxs-lookup"><span data-stu-id="dc8b1-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc8b1-106">S2</span><span class="sxs-lookup"><span data-stu-id="dc8b1-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc8b1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc8b1-107">DESCRIPTION</span></span>
<span data-ttu-id="dc8b1-108">Das Cmdlet " **Get-AzWebAppSlot** " Ruft Informationen zu einem Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="dc8b1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc8b1-109">EXAMPLES</span></span>

### <span data-ttu-id="dc8b1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc8b1-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="dc8b1-111">Dieser Befehl ruft den Steckplatz mit dem Namen Slot001 aus der Web-App mit dem Namen WebAppStandard ab, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="dc8b1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc8b1-112">PARAMETERS</span></span>

### <span data-ttu-id="dc8b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8b1-113">-DefaultProfile</span></span>
<span data-ttu-id="dc8b1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc8b1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="dc8b1-115">-Name</span></span>
<span data-ttu-id="dc8b1-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="dc8b1-116">WebApp Name</span></span>

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

### <span data-ttu-id="dc8b1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8b1-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc8b1-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="dc8b1-118">Resource Group Name</span></span>

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

### <span data-ttu-id="dc8b1-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="dc8b1-119">-Slot</span></span>
<span data-ttu-id="dc8b1-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="dc8b1-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc8b1-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="dc8b1-121">-WebApp</span></span>
<span data-ttu-id="dc8b1-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="dc8b1-122">WebApp Object</span></span>

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

### <span data-ttu-id="dc8b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8b1-123">CommonParameters</span></span>
<span data-ttu-id="dc8b1-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc8b1-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc8b1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8b1-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc8b1-126">INPUTS</span></span>

### <span data-ttu-id="dc8b1-127">Website</span><span class="sxs-lookup"><span data-stu-id="dc8b1-127">Site</span></span>
<span data-ttu-id="dc8b1-128">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="dc8b1-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc8b1-129">OUTPUTS</span></span>

## <span data-ttu-id="dc8b1-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc8b1-130">NOTES</span></span>

## <span data-ttu-id="dc8b1-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc8b1-131">RELATED LINKS</span></span>

[<span data-ttu-id="dc8b1-132">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc8b1-132">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="dc8b1-133">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc8b1-133">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="dc8b1-134">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc8b1-134">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="dc8b1-135">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc8b1-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="dc8b1-136">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc8b1-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="dc8b1-137">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc8b1-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="dc8b1-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dc8b1-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

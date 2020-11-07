---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 9f0e48b20d19113290784d65b6bc78531dc7b2a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842684"
---
# <span data-ttu-id="bdddc-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bdddc-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="bdddc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdddc-102">SYNOPSIS</span></span>

## <span data-ttu-id="bdddc-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdddc-103">SYNTAX</span></span>

### <span data-ttu-id="bdddc-104">S1</span><span class="sxs-lookup"><span data-stu-id="bdddc-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdddc-105">S2</span><span class="sxs-lookup"><span data-stu-id="bdddc-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdddc-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdddc-106">DESCRIPTION</span></span>
<span data-ttu-id="bdddc-107">Das Cmdlet " **Restart-AzWebAppSlot** " beendet den Azure Web App-Slot und startet dann.</span><span class="sxs-lookup"><span data-stu-id="bdddc-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="bdddc-108">Wenn sich der Web App-Slot im Zustand "beendet" befindet, verwenden Sie das Cmdlet "Start-AzWebAppSlot".</span><span class="sxs-lookup"><span data-stu-id="bdddc-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="bdddc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdddc-109">EXAMPLES</span></span>

### <span data-ttu-id="bdddc-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bdddc-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="bdddc-111">Mit diesem Befehl wird der Slot Slot001 für das Web-App-ContosoWebApp neu gestartet, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bdddc-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="bdddc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdddc-112">PARAMETERS</span></span>

### <span data-ttu-id="bdddc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdddc-113">-DefaultProfile</span></span>
<span data-ttu-id="bdddc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bdddc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdddc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bdddc-115">-Name</span></span>
<span data-ttu-id="bdddc-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="bdddc-116">WebApp Name</span></span>

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

### <span data-ttu-id="bdddc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdddc-117">-ResourceGroupName</span></span>
<span data-ttu-id="bdddc-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="bdddc-118">Resource Group Name</span></span>

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

### <span data-ttu-id="bdddc-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="bdddc-119">-Slot</span></span>
<span data-ttu-id="bdddc-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="bdddc-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bdddc-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="bdddc-121">-WebApp</span></span>
<span data-ttu-id="bdddc-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="bdddc-122">WebApp Object</span></span>

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

### <span data-ttu-id="bdddc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdddc-123">CommonParameters</span></span>
<span data-ttu-id="bdddc-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdddc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdddc-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdddc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdddc-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdddc-126">INPUTS</span></span>

### <span data-ttu-id="bdddc-127">Website</span><span class="sxs-lookup"><span data-stu-id="bdddc-127">Site</span></span>
<span data-ttu-id="bdddc-128">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bdddc-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bdddc-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdddc-129">OUTPUTS</span></span>

## <span data-ttu-id="bdddc-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdddc-130">NOTES</span></span>

## <span data-ttu-id="bdddc-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdddc-131">RELATED LINKS</span></span>

[<span data-ttu-id="bdddc-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bdddc-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="bdddc-133">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bdddc-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="bdddc-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bdddc-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="bdddc-135">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bdddc-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="bdddc-136">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bdddc-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="bdddc-137">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bdddc-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="bdddc-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bdddc-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

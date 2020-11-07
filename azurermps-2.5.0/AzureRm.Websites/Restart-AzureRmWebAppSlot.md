---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: ad3ff3dbd5589a890ecf7649c9a9b66843b8b444
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850504"
---
# <span data-ttu-id="a3e8e-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a3e8e-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="a3e8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3e8e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3e8e-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3e8e-103">SYNTAX</span></span>

### <span data-ttu-id="a3e8e-104">S1</span><span class="sxs-lookup"><span data-stu-id="a3e8e-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3e8e-105">S2</span><span class="sxs-lookup"><span data-stu-id="a3e8e-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3e8e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3e8e-106">DESCRIPTION</span></span>
<span data-ttu-id="a3e8e-107">Das Cmdlet " **Restart-AzureRmWebAppSlot** " beendet den Azure Web App-Slot und startet dann.</span><span class="sxs-lookup"><span data-stu-id="a3e8e-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="a3e8e-108">Wenn sich der Web App-Slot im Zustand "beendet" befindet, verwenden Sie das Cmdlet "Start-AzureRmWebAppSlot".</span><span class="sxs-lookup"><span data-stu-id="a3e8e-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="a3e8e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3e8e-109">EXAMPLES</span></span>

### <span data-ttu-id="a3e8e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3e8e-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="a3e8e-111">Mit diesem Befehl wird der Slot Slot001 für das Web-App-ContosoWebApp neu gestartet, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a3e8e-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="a3e8e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3e8e-112">PARAMETERS</span></span>

### <span data-ttu-id="a3e8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e8e-113">-DefaultProfile</span></span>
<span data-ttu-id="a3e8e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3e8e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e8e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a3e8e-115">-Name</span></span>
<span data-ttu-id="a3e8e-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="a3e8e-116">WebApp Name</span></span>

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

### <span data-ttu-id="a3e8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3e8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3e8e-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a3e8e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a3e8e-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="a3e8e-119">-Slot</span></span>
<span data-ttu-id="a3e8e-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="a3e8e-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a3e8e-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="a3e8e-121">-WebApp</span></span>
<span data-ttu-id="a3e8e-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="a3e8e-122">WebApp Object</span></span>

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

### <span data-ttu-id="a3e8e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e8e-123">CommonParameters</span></span>
<span data-ttu-id="a3e8e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3e8e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e8e-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3e8e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e8e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3e8e-126">INPUTS</span></span>

### <span data-ttu-id="a3e8e-127">Website</span><span class="sxs-lookup"><span data-stu-id="a3e8e-127">Site</span></span>
<span data-ttu-id="a3e8e-128">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3e8e-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a3e8e-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3e8e-129">OUTPUTS</span></span>

## <span data-ttu-id="a3e8e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3e8e-130">NOTES</span></span>

## <span data-ttu-id="a3e8e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3e8e-131">RELATED LINKS</span></span>

[<span data-ttu-id="a3e8e-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a3e8e-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="a3e8e-133">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a3e8e-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="a3e8e-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a3e8e-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="a3e8e-135">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a3e8e-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="a3e8e-136">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a3e8e-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="a3e8e-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a3e8e-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="a3e8e-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a3e8e-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

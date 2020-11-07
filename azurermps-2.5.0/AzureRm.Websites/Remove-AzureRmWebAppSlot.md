---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 93db0a86caf381b32293089bd68a6efafc20ef02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850208"
---
# <span data-ttu-id="9f538-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f538-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="9f538-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f538-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f538-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f538-103">SYNTAX</span></span>

### <span data-ttu-id="9f538-104">S1</span><span class="sxs-lookup"><span data-stu-id="9f538-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f538-105">S2</span><span class="sxs-lookup"><span data-stu-id="9f538-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f538-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f538-106">DESCRIPTION</span></span>
<span data-ttu-id="9f538-107">Mit dem Cmdlet **Remove-AzureRmWebAppSlot** wird ein Azure Web App-Steckplatz entfernt, vorausgesetzt, die Ressourcengruppe und der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="9f538-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="9f538-108">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="9f538-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="9f538-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f538-109">EXAMPLES</span></span>

### <span data-ttu-id="9f538-110">Beispiel 1: Entfernen eines Web App-Slots</span><span class="sxs-lookup"><span data-stu-id="9f538-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="9f538-111">Mit diesem Befehl wird der Steckplatz mit dem Namen "Slot001" entfernt, der Web App-ContosoSite zugeordnet ist, die zu der Ressourcengruppe "Default-Web-westus" gehört.</span><span class="sxs-lookup"><span data-stu-id="9f538-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="9f538-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f538-112">PARAMETERS</span></span>

### <span data-ttu-id="9f538-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f538-113">-DefaultProfile</span></span>
<span data-ttu-id="9f538-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9f538-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f538-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9f538-115">-Force</span></span>
<span data-ttu-id="9f538-116">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="9f538-116">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f538-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9f538-117">-Name</span></span>
<span data-ttu-id="9f538-118">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9f538-118">WebApp Name</span></span>

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

### <span data-ttu-id="9f538-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f538-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f538-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9f538-120">Resource Group Name</span></span>

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

### <span data-ttu-id="9f538-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="9f538-121">-Slot</span></span>
<span data-ttu-id="9f538-122">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="9f538-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="9f538-123">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="9f538-123">-WebApp</span></span>
<span data-ttu-id="9f538-124">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="9f538-124">WebApp Object</span></span>

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

### <span data-ttu-id="9f538-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9f538-125">-Confirm</span></span>
<span data-ttu-id="9f538-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f538-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f538-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f538-127">-WhatIf</span></span>
<span data-ttu-id="9f538-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f538-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f538-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f538-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="9f538-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f538-130">-AsJob</span></span>
<span data-ttu-id="9f538-131">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9f538-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f538-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f538-132">CommonParameters</span></span>
<span data-ttu-id="9f538-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f538-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f538-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f538-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f538-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f538-135">INPUTS</span></span>

### <span data-ttu-id="9f538-136">Website</span><span class="sxs-lookup"><span data-stu-id="9f538-136">Site</span></span>
<span data-ttu-id="9f538-137">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f538-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9f538-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f538-138">OUTPUTS</span></span>

### <span data-ttu-id="9f538-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9f538-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="9f538-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f538-140">NOTES</span></span>

## <span data-ttu-id="9f538-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f538-141">RELATED LINKS</span></span>

[<span data-ttu-id="9f538-142">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f538-142">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f538-143">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f538-143">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f538-144">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f538-144">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f538-145">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f538-145">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f538-146">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f538-146">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f538-147">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f538-147">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f538-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9f538-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 7fdf5e8de2ec326888c57e8219a006f9ef447aa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497177"
---
# <span data-ttu-id="48549-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48549-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="48549-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48549-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48549-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="48549-103">SYNTAX</span></span>

### <span data-ttu-id="48549-104">S1</span><span class="sxs-lookup"><span data-stu-id="48549-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48549-105">S2</span><span class="sxs-lookup"><span data-stu-id="48549-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48549-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48549-106">DESCRIPTION</span></span>
<span data-ttu-id="48549-107">Mit dem Cmdlet **Remove-AzureRmWebAppSlot** wird ein Azure Web App-Steckplatz entfernt, vorausgesetzt, die Ressourcengruppe und der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="48549-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="48549-108">Dieses Cmdlet entfernt standardmäßig auch alle Slots und Metriken.</span><span class="sxs-lookup"><span data-stu-id="48549-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="48549-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48549-109">EXAMPLES</span></span>

### <span data-ttu-id="48549-110">Beispiel 1: Entfernen eines Web App-Slots</span><span class="sxs-lookup"><span data-stu-id="48549-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="48549-111">Mit diesem Befehl wird der Steckplatz mit dem Namen "Slot001" entfernt, der Web App-ContosoSite zugeordnet ist, die zu der Ressourcengruppe "Default-Web-westus" gehört.</span><span class="sxs-lookup"><span data-stu-id="48549-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="48549-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="48549-112">PARAMETERS</span></span>

### <span data-ttu-id="48549-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48549-113">-AsJob</span></span>
<span data-ttu-id="48549-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="48549-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48549-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48549-115">-DefaultProfile</span></span>
<span data-ttu-id="48549-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="48549-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48549-117">-Force</span><span class="sxs-lookup"><span data-stu-id="48549-117">-Force</span></span>
<span data-ttu-id="48549-118">Option "gewaltsam entfernen"</span><span class="sxs-lookup"><span data-stu-id="48549-118">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48549-119">-Name</span><span class="sxs-lookup"><span data-stu-id="48549-119">-Name</span></span>
<span data-ttu-id="48549-120">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="48549-120">WebApp Name</span></span>

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

### <span data-ttu-id="48549-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48549-121">-ResourceGroupName</span></span>
<span data-ttu-id="48549-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="48549-122">Resource Group Name</span></span>

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

### <span data-ttu-id="48549-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="48549-123">-Slot</span></span>
<span data-ttu-id="48549-124">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="48549-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48549-125">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="48549-125">-WebApp</span></span>
<span data-ttu-id="48549-126">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="48549-126">WebApp Object</span></span>

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

### <span data-ttu-id="48549-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="48549-127">-Confirm</span></span>
<span data-ttu-id="48549-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48549-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48549-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48549-129">-WhatIf</span></span>
<span data-ttu-id="48549-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48549-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48549-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48549-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48549-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48549-132">CommonParameters</span></span>
<span data-ttu-id="48549-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48549-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48549-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48549-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48549-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48549-135">INPUTS</span></span>

### <span data-ttu-id="48549-136">System. String</span><span class="sxs-lookup"><span data-stu-id="48549-136">System.String</span></span>

### <span data-ttu-id="48549-137">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="48549-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="48549-138">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="48549-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="48549-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48549-139">OUTPUTS</span></span>

### <span data-ttu-id="48549-140">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="48549-140">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="48549-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="48549-141">NOTES</span></span>

## <span data-ttu-id="48549-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48549-142">RELATED LINKS</span></span>

[<span data-ttu-id="48549-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48549-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="48549-144">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48549-144">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="48549-145">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48549-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="48549-146">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48549-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="48549-147">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48549-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="48549-148">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48549-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="48549-149">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="48549-149">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

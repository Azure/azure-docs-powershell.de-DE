---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 75b8190c34d5335904d40d386cabc76e8cbf0b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476885"
---
# <span data-ttu-id="64a62-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="64a62-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="64a62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64a62-102">SYNOPSIS</span></span>
<span data-ttu-id="64a62-103">Startet ein Manuelles Upgrade der VMSS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="64a62-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64a62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64a62-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64a62-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64a62-105">DESCRIPTION</span></span>
<span data-ttu-id="64a62-106">Das Update-AzureRmVmssInstance-Cmdlet startet ein Manuelles Upgrade der angegebenen VMSS-Instanz (Virtual Machine Scale Sets).</span><span class="sxs-lookup"><span data-stu-id="64a62-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="64a62-107">Diese wird verwendet, wenn die Upgrade-Richtlinie für den VMSS-Skalierungs Satz auf manuell eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="64a62-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="64a62-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64a62-108">EXAMPLES</span></span>

### <span data-ttu-id="64a62-109">Beispiel 1: Starten eines Upgrades der VMSS-Instanz</span><span class="sxs-lookup"><span data-stu-id="64a62-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="64a62-110">Mit diesem Befehl wird ein Upgrade des VMSS namens VMScaleSet001 mit der Instanz-ID 0 gestartet.</span><span class="sxs-lookup"><span data-stu-id="64a62-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="64a62-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="64a62-111">PARAMETERS</span></span>

### <span data-ttu-id="64a62-112">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="64a62-112">-InstanceId</span></span>
<span data-ttu-id="64a62-113">Gibt als Zeichenfolgenarray die ID oder die IDs der Instanz an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64a62-113">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64a62-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a62-114">-ResourceGroupName</span></span>
<span data-ttu-id="64a62-115">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="64a62-115">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64a62-116">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="64a62-116">-VMScaleSetName</span></span>
<span data-ttu-id="64a62-117">Gibt den Namen der VMSS-Instanz an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="64a62-117">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64a62-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="64a62-118">-Confirm</span></span>
<span data-ttu-id="64a62-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64a62-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a62-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a62-120">-WhatIf</span></span>
<span data-ttu-id="64a62-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64a62-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="64a62-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64a62-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a62-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a62-123">CommonParameters</span></span>
<span data-ttu-id="64a62-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a62-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a62-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64a62-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a62-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64a62-126">INPUTS</span></span>

### <span data-ttu-id="64a62-127">Keine</span><span class="sxs-lookup"><span data-stu-id="64a62-127">None</span></span>
<span data-ttu-id="64a62-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="64a62-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64a62-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64a62-129">OUTPUTS</span></span>

###  
<span data-ttu-id="64a62-130">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="64a62-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="64a62-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="64a62-131">NOTES</span></span>

## <span data-ttu-id="64a62-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64a62-132">RELATED LINKS</span></span>

[<span data-ttu-id="64a62-133">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="64a62-133">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)



---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: d29bc2c479eb7799784a4e727764dc897fd715af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663184"
---
# <span data-ttu-id="38f34-101">Update-AzureRmVmssInstance</span><span class="sxs-lookup"><span data-stu-id="38f34-101">Update-AzureRmVmssInstance</span></span>

## <span data-ttu-id="38f34-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38f34-102">SYNOPSIS</span></span>
<span data-ttu-id="38f34-103">Startet ein Manuelles Upgrade der VMSS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="38f34-103">Starts a manual upgrade of the VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38f34-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38f34-104">SYNTAX</span></span>

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38f34-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38f34-105">DESCRIPTION</span></span>
<span data-ttu-id="38f34-106">Das Update-AzureRmVmssInstance-Cmdlet startet ein Manuelles Upgrade der angegebenen VMSS-Instanz (Virtual Machine Scale Sets).</span><span class="sxs-lookup"><span data-stu-id="38f34-106">The Update-AzureRmVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="38f34-107">Diese wird verwendet, wenn die Upgrade-Richtlinie für den VMSS-Skalierungs Satz auf manuell eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="38f34-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="38f34-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38f34-108">EXAMPLES</span></span>

### <span data-ttu-id="38f34-109">Beispiel 1: Starten eines Upgrades der VMSS-Instanz</span><span class="sxs-lookup"><span data-stu-id="38f34-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="38f34-110">Mit diesem Befehl wird ein Upgrade des VMSS namens VMScaleSet001 mit der Instanz-ID 0 gestartet.</span><span class="sxs-lookup"><span data-stu-id="38f34-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="38f34-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="38f34-111">PARAMETERS</span></span>

### <span data-ttu-id="38f34-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38f34-112">-AsJob</span></span>
<span data-ttu-id="38f34-113">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="38f34-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="38f34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f34-114">-DefaultProfile</span></span>
<span data-ttu-id="38f34-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38f34-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38f34-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="38f34-116">-InstanceId</span></span>
<span data-ttu-id="38f34-117">Gibt als Zeichenfolgenarray die ID oder die IDs der Instanz an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="38f34-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f34-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f34-118">-ResourceGroupName</span></span>
<span data-ttu-id="38f34-119">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="38f34-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f34-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="38f34-120">-VMScaleSetName</span></span>
<span data-ttu-id="38f34-121">Gibt den Namen der VMSS-Instanz an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="38f34-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f34-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="38f34-122">-Confirm</span></span>
<span data-ttu-id="38f34-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38f34-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f34-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f34-124">-WhatIf</span></span>
<span data-ttu-id="38f34-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38f34-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38f34-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38f34-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f34-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f34-127">CommonParameters</span></span>
<span data-ttu-id="38f34-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f34-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f34-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f34-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f34-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38f34-130">INPUTS</span></span>

### <span data-ttu-id="38f34-131">System. String</span><span class="sxs-lookup"><span data-stu-id="38f34-131">System.String</span></span>

### <span data-ttu-id="38f34-132">System. String []</span><span class="sxs-lookup"><span data-stu-id="38f34-132">System.String[]</span></span>

## <span data-ttu-id="38f34-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38f34-133">OUTPUTS</span></span>

### <span data-ttu-id="38f34-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="38f34-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="38f34-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="38f34-135">NOTES</span></span>

## <span data-ttu-id="38f34-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38f34-136">RELATED LINKS</span></span>

[<span data-ttu-id="38f34-137">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="38f34-137">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)



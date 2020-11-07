---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 27d1e45a9e2c85fb3d2f7470db97ce2426f62a19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850091"
---
# <span data-ttu-id="8b33c-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8b33c-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="8b33c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b33c-102">SYNOPSIS</span></span>
<span data-ttu-id="8b33c-103">Entfernt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="8b33c-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b33c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b33c-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b33c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b33c-105">DESCRIPTION</span></span>
<span data-ttu-id="8b33c-106">Das Cmdlet **Remove-AzureRmContainerService** entfernt einen Containerdienst aus Ihrem Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="8b33c-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="8b33c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b33c-107">EXAMPLES</span></span>

### <span data-ttu-id="8b33c-108">Beispiel 1: Entfernen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="8b33c-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="8b33c-109">Dieser Befehl entfernt den Containerdienst mit dem Namen CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="8b33c-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="8b33c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b33c-110">PARAMETERS</span></span>

### <span data-ttu-id="8b33c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b33c-111">-AsJob</span></span>
<span data-ttu-id="8b33c-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="8b33c-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8b33c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b33c-113">-DefaultProfile</span></span>
<span data-ttu-id="8b33c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b33c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b33c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8b33c-115">-Force</span></span>
<span data-ttu-id="8b33c-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8b33c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b33c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8b33c-117">-Name</span></span>
<span data-ttu-id="8b33c-118">Gibt den Namen des Container Diensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b33c-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b33c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b33c-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b33c-120">Gibt die Ressourcengruppe des Container Diensts an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8b33c-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8b33c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b33c-121">-Confirm</span></span>
<span data-ttu-id="8b33c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b33c-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="8b33c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b33c-123">-WhatIf</span></span>
<span data-ttu-id="8b33c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b33c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b33c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b33c-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="8b33c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b33c-126">CommonParameters</span></span>
<span data-ttu-id="8b33c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b33c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b33c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b33c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b33c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b33c-129">INPUTS</span></span>

### <span data-ttu-id="8b33c-130">Keine</span><span class="sxs-lookup"><span data-stu-id="8b33c-130">None</span></span>
<span data-ttu-id="8b33c-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8b33c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b33c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b33c-132">OUTPUTS</span></span>

### <span data-ttu-id="8b33c-133">System. void</span><span class="sxs-lookup"><span data-stu-id="8b33c-133">System.Void</span></span>

## <span data-ttu-id="8b33c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b33c-134">NOTES</span></span>

## <span data-ttu-id="8b33c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b33c-135">RELATED LINKS</span></span>

[<span data-ttu-id="8b33c-136">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8b33c-136">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="8b33c-137">Neu – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8b33c-137">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="8b33c-138">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8b33c-138">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)



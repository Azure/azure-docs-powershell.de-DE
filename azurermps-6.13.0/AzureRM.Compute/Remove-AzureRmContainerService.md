---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: 19c94fae0192766b87f430e6137fe8d3652325c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480449"
---
# <span data-ttu-id="12a15-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="12a15-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="12a15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12a15-102">SYNOPSIS</span></span>
<span data-ttu-id="12a15-103">Entfernt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="12a15-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12a15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12a15-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12a15-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12a15-105">DESCRIPTION</span></span>
<span data-ttu-id="12a15-106">Das Cmdlet **Remove-AzureRmContainerService** entfernt einen Containerdienst aus Ihrem Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="12a15-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="12a15-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12a15-107">EXAMPLES</span></span>

### <span data-ttu-id="12a15-108">Beispiel 1: Entfernen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="12a15-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="12a15-109">Dieser Befehl entfernt den Containerdienst mit dem Namen CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="12a15-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="12a15-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="12a15-110">PARAMETERS</span></span>

### <span data-ttu-id="12a15-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12a15-111">-AsJob</span></span>
<span data-ttu-id="12a15-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="12a15-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="12a15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a15-113">-DefaultProfile</span></span>
<span data-ttu-id="12a15-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12a15-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12a15-115">-Force</span><span class="sxs-lookup"><span data-stu-id="12a15-115">-Force</span></span>
<span data-ttu-id="12a15-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="12a15-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12a15-117">-Name</span><span class="sxs-lookup"><span data-stu-id="12a15-117">-Name</span></span>
<span data-ttu-id="12a15-118">Gibt den Namen des Container Diensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="12a15-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a15-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a15-119">-ResourceGroupName</span></span>
<span data-ttu-id="12a15-120">Gibt die Ressourcengruppe des Container Diensts an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="12a15-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12a15-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12a15-121">-Confirm</span></span>
<span data-ttu-id="12a15-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12a15-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12a15-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12a15-123">-WhatIf</span></span>
<span data-ttu-id="12a15-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12a15-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12a15-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12a15-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12a15-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a15-126">CommonParameters</span></span>
<span data-ttu-id="12a15-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a15-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a15-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a15-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a15-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12a15-129">INPUTS</span></span>

### <span data-ttu-id="12a15-130">System. String</span><span class="sxs-lookup"><span data-stu-id="12a15-130">System.String</span></span>

## <span data-ttu-id="12a15-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12a15-131">OUTPUTS</span></span>

### <span data-ttu-id="12a15-132">System. void</span><span class="sxs-lookup"><span data-stu-id="12a15-132">System.Void</span></span>

## <span data-ttu-id="12a15-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="12a15-133">NOTES</span></span>

## <span data-ttu-id="12a15-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12a15-134">RELATED LINKS</span></span>

[<span data-ttu-id="12a15-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="12a15-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="12a15-136">Neu – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="12a15-136">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="12a15-137">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="12a15-137">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)



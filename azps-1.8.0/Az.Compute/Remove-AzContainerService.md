---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: e41817c76cbc35564f5eec408de8acecac0466c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661498"
---
# <span data-ttu-id="26d90-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="26d90-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="26d90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26d90-102">SYNOPSIS</span></span>
<span data-ttu-id="26d90-103">Entfernt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="26d90-103">Removes a container service.</span></span>

## <span data-ttu-id="26d90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26d90-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26d90-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26d90-105">DESCRIPTION</span></span>
<span data-ttu-id="26d90-106">Das Cmdlet **Remove-AzContainerService** entfernt einen Containerdienst aus Ihrem Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="26d90-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="26d90-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26d90-107">EXAMPLES</span></span>

### <span data-ttu-id="26d90-108">Beispiel 1: Entfernen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="26d90-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="26d90-109">Dieser Befehl entfernt den Containerdienst mit dem Namen CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="26d90-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="26d90-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="26d90-110">PARAMETERS</span></span>

### <span data-ttu-id="26d90-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26d90-111">-AsJob</span></span>
<span data-ttu-id="26d90-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="26d90-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="26d90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26d90-113">-DefaultProfile</span></span>
<span data-ttu-id="26d90-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26d90-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d90-115">-Force</span><span class="sxs-lookup"><span data-stu-id="26d90-115">-Force</span></span>
<span data-ttu-id="26d90-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="26d90-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26d90-117">-Name</span><span class="sxs-lookup"><span data-stu-id="26d90-117">-Name</span></span>
<span data-ttu-id="26d90-118">Gibt den Namen des Container Diensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="26d90-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="26d90-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26d90-119">-ResourceGroupName</span></span>
<span data-ttu-id="26d90-120">Gibt die Ressourcengruppe des Container Diensts an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="26d90-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26d90-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26d90-121">-Confirm</span></span>
<span data-ttu-id="26d90-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26d90-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26d90-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26d90-123">-WhatIf</span></span>
<span data-ttu-id="26d90-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26d90-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26d90-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26d90-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26d90-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26d90-126">CommonParameters</span></span>
<span data-ttu-id="26d90-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26d90-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26d90-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26d90-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26d90-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26d90-129">INPUTS</span></span>

### <span data-ttu-id="26d90-130">System. String</span><span class="sxs-lookup"><span data-stu-id="26d90-130">System.String</span></span>

## <span data-ttu-id="26d90-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26d90-131">OUTPUTS</span></span>

### <span data-ttu-id="26d90-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="26d90-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="26d90-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="26d90-133">NOTES</span></span>

## <span data-ttu-id="26d90-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26d90-134">RELATED LINKS</span></span>

[<span data-ttu-id="26d90-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="26d90-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="26d90-136">Neu – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="26d90-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="26d90-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="26d90-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 4a83b1c23b3c0cb9cdd86fde6f8aac4bb13f91ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844432"
---
# <span data-ttu-id="cda95-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="cda95-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="cda95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cda95-102">SYNOPSIS</span></span>
<span data-ttu-id="cda95-103">Entfernt einen Containerdienst.</span><span class="sxs-lookup"><span data-stu-id="cda95-103">Removes a container service.</span></span>

## <span data-ttu-id="cda95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cda95-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cda95-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cda95-105">DESCRIPTION</span></span>
<span data-ttu-id="cda95-106">Das Cmdlet **Remove-AzContainerService** entfernt einen Containerdienst aus Ihrem Azure-Konto.</span><span class="sxs-lookup"><span data-stu-id="cda95-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="cda95-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cda95-107">EXAMPLES</span></span>

### <span data-ttu-id="cda95-108">Beispiel 1: Entfernen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="cda95-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="cda95-109">Dieser Befehl entfernt den Containerdienst mit dem Namen CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="cda95-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="cda95-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cda95-110">PARAMETERS</span></span>

### <span data-ttu-id="cda95-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cda95-111">-AsJob</span></span>
<span data-ttu-id="cda95-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="cda95-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cda95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda95-113">-DefaultProfile</span></span>
<span data-ttu-id="cda95-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cda95-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cda95-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cda95-115">-Force</span></span>
<span data-ttu-id="cda95-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="cda95-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cda95-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cda95-117">-Name</span></span>
<span data-ttu-id="cda95-118">Gibt den Namen des Container Diensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="cda95-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cda95-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda95-119">-ResourceGroupName</span></span>
<span data-ttu-id="cda95-120">Gibt die Ressourcengruppe des Container Diensts an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="cda95-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cda95-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cda95-121">-Confirm</span></span>
<span data-ttu-id="cda95-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cda95-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="cda95-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda95-123">-WhatIf</span></span>
<span data-ttu-id="cda95-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cda95-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cda95-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cda95-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="cda95-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda95-126">CommonParameters</span></span>
<span data-ttu-id="cda95-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda95-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda95-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cda95-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda95-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cda95-129">INPUTS</span></span>

### <span data-ttu-id="cda95-130">Keine</span><span class="sxs-lookup"><span data-stu-id="cda95-130">None</span></span>
<span data-ttu-id="cda95-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="cda95-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cda95-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cda95-132">OUTPUTS</span></span>

### <span data-ttu-id="cda95-133">System. void</span><span class="sxs-lookup"><span data-stu-id="cda95-133">System.Void</span></span>

## <span data-ttu-id="cda95-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="cda95-134">NOTES</span></span>

## <span data-ttu-id="cda95-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cda95-135">RELATED LINKS</span></span>

[<span data-ttu-id="cda95-136">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="cda95-136">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="cda95-137">Neu – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="cda95-137">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="cda95-138">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="cda95-138">Update-AzContainerService</span></span>](./Update-AzContainerService.md)



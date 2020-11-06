---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: 3cc48d103867008b247ce480de43d1ccadc68d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500877"
---
# <span data-ttu-id="8d9ae-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d9ae-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="8d9ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9ae-103">Entfernt einen virtuellen Computer aus Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d9ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d9ae-104">SYNTAX</span></span>

### <span data-ttu-id="8d9ae-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8d9ae-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d9ae-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8d9ae-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d9ae-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d9ae-107">DESCRIPTION</span></span>
<span data-ttu-id="8d9ae-108">Das Cmdlet **Remove-AzureRmVM** entfernt einen virtuellen Computer aus Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="8d9ae-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d9ae-109">EXAMPLES</span></span>

### <span data-ttu-id="8d9ae-110">Beispiel 1: Entfernen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="8d9ae-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8d9ae-111">Dieser Befehl entfernt den virtuellen Computer mit dem Namen VirtualMachine07 in der Ressourcengruppe ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="8d9ae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d9ae-112">PARAMETERS</span></span>

### <span data-ttu-id="8d9ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9ae-113">-DefaultProfile</span></span>
<span data-ttu-id="8d9ae-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d9ae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8d9ae-115">-Force</span></span>
<span data-ttu-id="8d9ae-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9ae-117">-ID</span><span class="sxs-lookup"><span data-stu-id="8d9ae-117">-Id</span></span>
<span data-ttu-id="8d9ae-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9ae-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8d9ae-119">-Name</span></span>
<span data-ttu-id="8d9ae-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d9ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d9ae-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9ae-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d9ae-123">-Confirm</span></span>
<span data-ttu-id="8d9ae-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d9ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d9ae-125">-WhatIf</span></span>
<span data-ttu-id="8d9ae-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8d9ae-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d9ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9ae-128">CommonParameters</span></span>
<span data-ttu-id="8d9ae-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d9ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9ae-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d9ae-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9ae-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d9ae-131">INPUTS</span></span>

## <span data-ttu-id="8d9ae-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d9ae-132">OUTPUTS</span></span>

## <span data-ttu-id="8d9ae-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d9ae-133">NOTES</span></span>

## <span data-ttu-id="8d9ae-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d9ae-134">RELATED LINKS</span></span>

[<span data-ttu-id="8d9ae-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d9ae-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8d9ae-136">Neu – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d9ae-136">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="8d9ae-137">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d9ae-137">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="8d9ae-138">Anfang-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d9ae-138">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="8d9ae-139">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d9ae-139">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="8d9ae-140">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8d9ae-140">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)



---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 3091cb877ff792527cf97e3d44b7c363f9dd94b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479358"
---
# <span data-ttu-id="95bc4-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bc4-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="95bc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="95bc4-103">Startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="95bc4-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95bc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95bc4-104">SYNTAX</span></span>

### <span data-ttu-id="95bc4-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="95bc4-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95bc4-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="95bc4-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95bc4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95bc4-107">DESCRIPTION</span></span>
<span data-ttu-id="95bc4-108">Das Cmdlet **Start-AzureRmVM** startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="95bc4-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="95bc4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95bc4-109">EXAMPLES</span></span>

### <span data-ttu-id="95bc4-110">Beispiel 1: Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="95bc4-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="95bc4-111">Dieser Befehl startet den virtuellen Computer mit dem Namen VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="95bc4-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="95bc4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="95bc4-112">PARAMETERS</span></span>

### <span data-ttu-id="95bc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95bc4-113">-DefaultProfile</span></span>
<span data-ttu-id="95bc4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95bc4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95bc4-115">-ID</span><span class="sxs-lookup"><span data-stu-id="95bc4-115">-Id</span></span>
<span data-ttu-id="95bc4-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="95bc4-116">The resource group name.</span></span>

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

### <span data-ttu-id="95bc4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="95bc4-117">-Name</span></span>
<span data-ttu-id="95bc4-118">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="95bc4-118">The virtual machine name.</span></span>

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

### <span data-ttu-id="95bc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95bc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="95bc4-120">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="95bc4-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="95bc4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95bc4-121">-Confirm</span></span>
<span data-ttu-id="95bc4-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95bc4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95bc4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95bc4-123">-WhatIf</span></span>
<span data-ttu-id="95bc4-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95bc4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95bc4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95bc4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95bc4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bc4-126">CommonParameters</span></span>
<span data-ttu-id="95bc4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95bc4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95bc4-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95bc4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bc4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95bc4-129">INPUTS</span></span>

## <span data-ttu-id="95bc4-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95bc4-130">OUTPUTS</span></span>

## <span data-ttu-id="95bc4-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="95bc4-131">NOTES</span></span>

## <span data-ttu-id="95bc4-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95bc4-132">RELATED LINKS</span></span>

[<span data-ttu-id="95bc4-133">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bc4-133">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="95bc4-134">Neu – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bc4-134">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="95bc4-135">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bc4-135">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="95bc4-136">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bc4-136">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="95bc4-137">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bc4-137">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="95bc4-138">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bc4-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)



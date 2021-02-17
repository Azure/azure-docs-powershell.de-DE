---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169716"
---
# <span data-ttu-id="74f05-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="74f05-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="74f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74f05-102">SYNOPSIS</span></span>
<span data-ttu-id="74f05-103">Entfernt eine Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="74f05-103">Removes an application security group.</span></span>

## <span data-ttu-id="74f05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74f05-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74f05-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74f05-105">DESCRIPTION</span></span>
<span data-ttu-id="74f05-106">Das **Cmdlet "Remove-AzApplicationSecurityGroup"** entfernt eine Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="74f05-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="74f05-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74f05-107">EXAMPLES</span></span>

### <span data-ttu-id="74f05-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74f05-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="74f05-109">Mit diesem Befehl wird eine Anwendungssicherheitsgruppe mit dem Namen "MyApplicationSecurityGrouo" in der Ressourcengruppe "MyResourceGroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="74f05-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="74f05-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74f05-110">PARAMETERS</span></span>

### <span data-ttu-id="74f05-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74f05-111">-AsJob</span></span>
<span data-ttu-id="74f05-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="74f05-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74f05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f05-113">-DefaultProfile</span></span>
<span data-ttu-id="74f05-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74f05-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74f05-115">-Force</span><span class="sxs-lookup"><span data-stu-id="74f05-115">-Force</span></span>
<span data-ttu-id="74f05-116">Bestätigen Sie nicht, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="74f05-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="74f05-117">-Name</span><span class="sxs-lookup"><span data-stu-id="74f05-117">-Name</span></span>
<span data-ttu-id="74f05-118">Der Name der Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="74f05-118">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f05-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74f05-119">-PassThru</span></span>
<span data-ttu-id="74f05-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="74f05-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="74f05-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="74f05-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74f05-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f05-122">-ResourceGroupName</span></span>
<span data-ttu-id="74f05-123">Der Ressourcengruppenname der Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="74f05-123">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f05-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74f05-124">-Confirm</span></span>
<span data-ttu-id="74f05-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74f05-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74f05-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="74f05-126">-WhatIf</span></span>
<span data-ttu-id="74f05-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74f05-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74f05-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74f05-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74f05-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f05-129">CommonParameters</span></span>
<span data-ttu-id="74f05-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f05-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f05-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f05-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f05-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74f05-132">INPUTS</span></span>

### <span data-ttu-id="74f05-133">System.String</span><span class="sxs-lookup"><span data-stu-id="74f05-133">System.String</span></span>

## <span data-ttu-id="74f05-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74f05-134">OUTPUTS</span></span>

### <span data-ttu-id="74f05-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74f05-135">System.Boolean</span></span>

## <span data-ttu-id="74f05-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74f05-136">NOTES</span></span>

## <span data-ttu-id="74f05-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74f05-137">RELATED LINKS</span></span>

[<span data-ttu-id="74f05-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="74f05-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="74f05-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="74f05-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

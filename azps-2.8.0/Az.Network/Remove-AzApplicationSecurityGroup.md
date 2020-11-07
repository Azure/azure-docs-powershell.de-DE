---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 0af35c08cce181ba96f15ca77c0f17f96cfeb32e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821404"
---
# <span data-ttu-id="952b3-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="952b3-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="952b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="952b3-102">SYNOPSIS</span></span>
<span data-ttu-id="952b3-103">Entfernt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="952b3-103">Removes an application security group.</span></span>

## <span data-ttu-id="952b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="952b3-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="952b3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="952b3-105">DESCRIPTION</span></span>
<span data-ttu-id="952b3-106">Das Cmdlet " **Remove-AzApplicationSecurityGroup** " entfernt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="952b3-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="952b3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="952b3-107">EXAMPLES</span></span>

### <span data-ttu-id="952b3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="952b3-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="952b3-109">Mit diesem Befehl wird eine Anwendungs Sicherheitsgruppe namens "MyApplicationSecurityGrouo" in der Ressourcengruppe "myresourcegroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="952b3-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="952b3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="952b3-110">PARAMETERS</span></span>

### <span data-ttu-id="952b3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="952b3-111">-AsJob</span></span>
<span data-ttu-id="952b3-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="952b3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="952b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="952b3-113">-DefaultProfile</span></span>
<span data-ttu-id="952b3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="952b3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="952b3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="952b3-115">-Force</span></span>
<span data-ttu-id="952b3-116">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="952b3-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="952b3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="952b3-117">-Name</span></span>
<span data-ttu-id="952b3-118">Der Name der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="952b3-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="952b3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="952b3-119">-PassThru</span></span>
<span data-ttu-id="952b3-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="952b3-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="952b3-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="952b3-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="952b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="952b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="952b3-123">Der Ressourcengruppenname der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="952b3-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="952b3-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="952b3-124">-Confirm</span></span>
<span data-ttu-id="952b3-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="952b3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="952b3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="952b3-126">-WhatIf</span></span>
<span data-ttu-id="952b3-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="952b3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="952b3-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="952b3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="952b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952b3-129">CommonParameters</span></span>
<span data-ttu-id="952b3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="952b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952b3-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="952b3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952b3-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="952b3-132">INPUTS</span></span>

### <span data-ttu-id="952b3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="952b3-133">System.String</span></span>

## <span data-ttu-id="952b3-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="952b3-134">OUTPUTS</span></span>

### <span data-ttu-id="952b3-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="952b3-135">System.Boolean</span></span>

## <span data-ttu-id="952b3-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="952b3-136">NOTES</span></span>

## <span data-ttu-id="952b3-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="952b3-137">RELATED LINKS</span></span>

[<span data-ttu-id="952b3-138">Neu – AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="952b3-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="952b3-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="952b3-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176167"
---
# <span data-ttu-id="b5c96-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b5c96-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="b5c96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5c96-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c96-103">Entfernt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b5c96-103">Removes an application security group.</span></span>

## <span data-ttu-id="b5c96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5c96-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5c96-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5c96-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c96-106">Das Cmdlet " **Remove-AzApplicationSecurityGroup** " entfernt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b5c96-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="b5c96-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5c96-107">EXAMPLES</span></span>

### <span data-ttu-id="b5c96-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b5c96-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b5c96-109">Mit diesem Befehl wird eine Anwendungs Sicherheitsgruppe namens "MyApplicationSecurityGrouo" in der Ressourcengruppe "myresourcegroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b5c96-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="b5c96-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5c96-110">PARAMETERS</span></span>

### <span data-ttu-id="b5c96-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5c96-111">-AsJob</span></span>
<span data-ttu-id="b5c96-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b5c96-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5c96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c96-113">-DefaultProfile</span></span>
<span data-ttu-id="b5c96-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5c96-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5c96-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b5c96-115">-Force</span></span>
<span data-ttu-id="b5c96-116">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="b5c96-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="b5c96-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b5c96-117">-Name</span></span>
<span data-ttu-id="b5c96-118">Der Name der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b5c96-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="b5c96-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5c96-119">-PassThru</span></span>
<span data-ttu-id="b5c96-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b5c96-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b5c96-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b5c96-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5c96-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c96-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5c96-123">Der Ressourcengruppenname der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b5c96-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="b5c96-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b5c96-124">-Confirm</span></span>
<span data-ttu-id="b5c96-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5c96-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5c96-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c96-126">-WhatIf</span></span>
<span data-ttu-id="b5c96-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5c96-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5c96-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5c96-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5c96-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c96-129">CommonParameters</span></span>
<span data-ttu-id="b5c96-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c96-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c96-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c96-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c96-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5c96-132">INPUTS</span></span>

### <span data-ttu-id="b5c96-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b5c96-133">System.String</span></span>

## <span data-ttu-id="b5c96-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5c96-134">OUTPUTS</span></span>

### <span data-ttu-id="b5c96-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5c96-135">System.Boolean</span></span>

## <span data-ttu-id="b5c96-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5c96-136">NOTES</span></span>

## <span data-ttu-id="b5c96-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5c96-137">RELATED LINKS</span></span>

[<span data-ttu-id="b5c96-138">Neu – AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b5c96-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b5c96-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b5c96-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

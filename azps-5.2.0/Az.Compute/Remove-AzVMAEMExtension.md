---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358642"
---
# <span data-ttu-id="cf03c-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cf03c-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="cf03c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf03c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf03c-103">Entfernt die AEM-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="cf03c-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="cf03c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf03c-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf03c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf03c-105">DESCRIPTION</span></span>
<span data-ttu-id="cf03c-106">Das **Cmdlet "Remove-AzVMAEMExtension"** entfernt die Azure Enhanced Monitoring (AEM)-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="cf03c-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="cf03c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf03c-107">EXAMPLES</span></span>

### <span data-ttu-id="cf03c-108">Beispiel 1: Entfernen der Erweiterung AEM</span><span class="sxs-lookup"><span data-stu-id="cf03c-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="cf03c-109">Mit diesem Befehl wird die AEM-Erweiterung für den virtuellen Computer "contoso-server" entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf03c-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="cf03c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf03c-110">PARAMETERS</span></span>

### <span data-ttu-id="cf03c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf03c-111">-DefaultProfile</span></span>
<span data-ttu-id="cf03c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf03c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf03c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cf03c-113">-Name</span></span>
<span data-ttu-id="cf03c-114">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die Erweiterung AEM entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf03c-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf03c-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cf03c-115">-NoWait</span></span>
<span data-ttu-id="cf03c-116">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="cf03c-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="cf03c-117">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="cf03c-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cf03c-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="cf03c-118">-OSType</span></span>
<span data-ttu-id="cf03c-119">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="cf03c-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="cf03c-120">Wenn der Betriebssystemdatenträger keinen Typ hat, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="cf03c-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="cf03c-121">Die zulässigen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="cf03c-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf03c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf03c-122">-ResourceGroupName</span></span>
<span data-ttu-id="cf03c-123">Gibt den Namen der Ressourcengruppe eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="cf03c-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="cf03c-124">Mit diesem Cmdlet wird die Erweiterung AEM von diesem virtuellen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf03c-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="cf03c-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="cf03c-125">-VMName</span></span>
<span data-ttu-id="cf03c-126">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="cf03c-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cf03c-127">Dieses Cmdlet entfernt die "AEM"-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cf03c-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf03c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf03c-128">CommonParameters</span></span>
<span data-ttu-id="cf03c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf03c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf03c-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf03c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf03c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf03c-131">INPUTS</span></span>

### <span data-ttu-id="cf03c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="cf03c-132">System.String</span></span>

## <span data-ttu-id="cf03c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf03c-133">OUTPUTS</span></span>

### <span data-ttu-id="cf03c-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cf03c-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cf03c-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cf03c-135">NOTES</span></span>

## <span data-ttu-id="cf03c-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cf03c-136">RELATED LINKS</span></span>

[<span data-ttu-id="cf03c-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cf03c-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="cf03c-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cf03c-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="cf03c-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cf03c-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)



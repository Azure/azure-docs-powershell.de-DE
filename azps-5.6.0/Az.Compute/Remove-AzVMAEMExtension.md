---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 71fcf62049cfb15e830b4c8c5f311c042de55bb9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921395"
---
# <span data-ttu-id="3a3f6-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3a3f6-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="3a3f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3f6-103">Entfernt die AEM-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="3a3f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a3f6-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a3f6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a3f6-105">DESCRIPTION</span></span>
<span data-ttu-id="3a3f6-106">Das **Cmdlet Remove-AzVMAEMExtension** entfernt die Azure Enhanced Monitoring (AEM)-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="3a3f6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a3f6-107">EXAMPLES</span></span>

### <span data-ttu-id="3a3f6-108">Beispiel 1: Entfernen der Erweiterung AEM</span><span class="sxs-lookup"><span data-stu-id="3a3f6-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="3a3f6-109">Mit diesem Befehl wird die AEM-Erweiterung für den virtuellen Computer namens contoso-server entfernt.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="3a3f6-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3a3f6-110">PARAMETERS</span></span>

### <span data-ttu-id="3a3f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3f6-111">-DefaultProfile</span></span>
<span data-ttu-id="3a3f6-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a3f6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3a3f6-113">-Name</span></span>
<span data-ttu-id="3a3f6-114">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die Erweiterung AEM entfernt.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="3a3f6-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3a3f6-115">-NoWait</span></span>
<span data-ttu-id="3a3f6-116">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3a3f6-117">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3a3f6-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="3a3f6-118">-OSType</span></span>
<span data-ttu-id="3a3f6-119">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="3a3f6-120">Wenn der Betriebssystemdatenträger keinen Typ hat, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="3a3f6-121">Die zulässigen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="3a3f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="3a3f6-123">Gibt den Namen der Ressourcengruppe eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="3a3f6-124">Dieses Cmdlet entfernt die AEM-Erweiterung von diesem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="3a3f6-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="3a3f6-125">-VMName</span></span>
<span data-ttu-id="3a3f6-126">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3a3f6-127">Dieses Cmdlet entfernt die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a3f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3f6-128">CommonParameters</span></span>
<span data-ttu-id="3a3f6-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3f6-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a3f6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3f6-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a3f6-131">INPUTS</span></span>

### <span data-ttu-id="3a3f6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3a3f6-132">System.String</span></span>

## <span data-ttu-id="3a3f6-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a3f6-133">OUTPUTS</span></span>

### <span data-ttu-id="3a3f6-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3a3f6-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3a3f6-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3a3f6-135">NOTES</span></span>

## <span data-ttu-id="3a3f6-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3a3f6-136">RELATED LINKS</span></span>

[<span data-ttu-id="3a3f6-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3a3f6-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="3a3f6-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3a3f6-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="3a3f6-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3a3f6-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)



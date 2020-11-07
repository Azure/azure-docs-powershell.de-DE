---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 343ecb5159b252c97af05cffc89152e05028583b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652011"
---
# <span data-ttu-id="b11e4-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b11e4-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="b11e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b11e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b11e4-103">Entfernt die AEM-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="b11e4-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="b11e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b11e4-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b11e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b11e4-105">DESCRIPTION</span></span>
<span data-ttu-id="b11e4-106">Das Cmdlet **Remove-AzVMAEMExtension** entfernt die Erweiterung Azure Enhanced Monitoring (AEM) von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="b11e4-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="b11e4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b11e4-107">EXAMPLES</span></span>

### <span data-ttu-id="b11e4-108">Beispiel 1: Entfernen der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="b11e4-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="b11e4-109">Dieser Befehl entfernt die AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="b11e4-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="b11e4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b11e4-110">PARAMETERS</span></span>

### <span data-ttu-id="b11e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11e4-111">-DefaultProfile</span></span>
<span data-ttu-id="b11e4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b11e4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b11e4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b11e4-113">-Name</span></span>
<span data-ttu-id="b11e4-114">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die AEM-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="b11e4-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="b11e4-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b11e4-115">-NoWait</span></span>
<span data-ttu-id="b11e4-116">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="b11e4-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b11e4-117">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b11e4-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="b11e4-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="b11e4-118">-OSType</span></span>
<span data-ttu-id="b11e4-119">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b11e4-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="b11e4-120">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="b11e4-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="b11e4-121">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="b11e4-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="b11e4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b11e4-122">-ResourceGroupName</span></span>
<span data-ttu-id="b11e4-123">Gibt den Namen der Ressourcengruppe einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="b11e4-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="b11e4-124">Dieses Cmdlet entfernt die AEM-Erweiterung von dieser virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="b11e4-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="b11e4-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="b11e4-125">-VMName</span></span>
<span data-ttu-id="b11e4-126">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="b11e4-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b11e4-127">Dieses Cmdlet entfernt die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b11e4-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="b11e4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11e4-128">CommonParameters</span></span>
<span data-ttu-id="b11e4-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b11e4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11e4-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b11e4-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11e4-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b11e4-131">INPUTS</span></span>

### <span data-ttu-id="b11e4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b11e4-132">System.String</span></span>

## <span data-ttu-id="b11e4-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b11e4-133">OUTPUTS</span></span>

### <span data-ttu-id="b11e4-134">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b11e4-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b11e4-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b11e4-135">NOTES</span></span>

## <span data-ttu-id="b11e4-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b11e4-136">RELATED LINKS</span></span>

[<span data-ttu-id="b11e4-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b11e4-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="b11e4-138">Satz-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b11e4-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="b11e4-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b11e4-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)



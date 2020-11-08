---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165876"
---
# <span data-ttu-id="7af20-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7af20-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="7af20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7af20-102">SYNOPSIS</span></span>
<span data-ttu-id="7af20-103">Entfernt die AEM-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7af20-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="7af20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7af20-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7af20-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7af20-105">DESCRIPTION</span></span>
<span data-ttu-id="7af20-106">Das Cmdlet **Remove-AzVMAEMExtension** entfernt die Erweiterung Azure Enhanced Monitoring (AEM) von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7af20-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="7af20-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7af20-107">EXAMPLES</span></span>

### <span data-ttu-id="7af20-108">Beispiel 1: Entfernen der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7af20-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="7af20-109">Dieser Befehl entfernt die AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="7af20-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="7af20-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7af20-110">PARAMETERS</span></span>

### <span data-ttu-id="7af20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af20-111">-DefaultProfile</span></span>
<span data-ttu-id="7af20-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7af20-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7af20-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7af20-113">-Name</span></span>
<span data-ttu-id="7af20-114">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die AEM-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="7af20-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="7af20-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7af20-115">-NoWait</span></span>
<span data-ttu-id="7af20-116">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="7af20-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7af20-117">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7af20-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7af20-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="7af20-118">-OSType</span></span>
<span data-ttu-id="7af20-119">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="7af20-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="7af20-120">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="7af20-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="7af20-121">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="7af20-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="7af20-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7af20-122">-ResourceGroupName</span></span>
<span data-ttu-id="7af20-123">Gibt den Namen der Ressourcengruppe einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="7af20-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="7af20-124">Dieses Cmdlet entfernt die AEM-Erweiterung von dieser virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="7af20-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="7af20-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="7af20-125">-VMName</span></span>
<span data-ttu-id="7af20-126">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="7af20-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7af20-127">Dieses Cmdlet entfernt die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7af20-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="7af20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af20-128">CommonParameters</span></span>
<span data-ttu-id="7af20-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7af20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af20-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7af20-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af20-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7af20-131">INPUTS</span></span>

### <span data-ttu-id="7af20-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7af20-132">System.String</span></span>

## <span data-ttu-id="7af20-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7af20-133">OUTPUTS</span></span>

### <span data-ttu-id="7af20-134">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7af20-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7af20-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="7af20-135">NOTES</span></span>

## <span data-ttu-id="7af20-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7af20-136">RELATED LINKS</span></span>

[<span data-ttu-id="7af20-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7af20-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="7af20-138">Satz-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7af20-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="7af20-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7af20-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)



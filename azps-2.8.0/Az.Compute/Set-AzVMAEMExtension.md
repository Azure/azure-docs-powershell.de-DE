---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: deaa8470a4af38eba1f38581e03165c19b3b18f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651934"
---
# <span data-ttu-id="0bf1d-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0bf1d-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="0bf1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0bf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf1d-103">Ermöglicht die Unterstützung für die Überwachung von SAP-Systemen.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="0bf1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bf1d-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bf1d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bf1d-105">DESCRIPTION</span></span>
<span data-ttu-id="0bf1d-106">Das Cmdlet " **Satz-AzVMAEMExtension** " aktualisiert die Konfiguration einer virtuellen Maschine, um die Unterstützung für die Überwachung von SAP-Systemen zu aktivieren oder zu aktualisieren, die auf dem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="0bf1d-107">Das Cmdlet installiert die Erweiterung Azure Enhanced Monitoring (AEM), die die Leistungsdaten erfasst und für das SAP-System auffindbar macht.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="0bf1d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0bf1d-108">EXAMPLES</span></span>

### <span data-ttu-id="0bf1d-109">Beispiel 1: Verwenden der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="0bf1d-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="0bf1d-110">Dieser Befehl konfiguriert den virtuellen Computer mit dem Namen "Contoso-Server", um die AEM-Erweiterung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="0bf1d-111">Der Befehl gibt das Speicherkonto mit dem Namen "stdstorage" an.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="0bf1d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bf1d-112">PARAMETERS</span></span>

### <span data-ttu-id="0bf1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf1d-113">-DefaultProfile</span></span>
<span data-ttu-id="0bf1d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bf1d-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="0bf1d-115">-EnableWAD</span></span>
<span data-ttu-id="0bf1d-116">Wenn dieser Parameter bereitgestellt wird, aktiviert der Unifiedgroup Windows Azure-Diagnose für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf1d-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0bf1d-117">-NoWait</span></span>
<span data-ttu-id="0bf1d-118">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-118">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0bf1d-119">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-119">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0bf1d-120">-OSType</span><span class="sxs-lookup"><span data-stu-id="0bf1d-120">-OSType</span></span>
<span data-ttu-id="0bf1d-121">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-121">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="0bf1d-122">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-122">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="0bf1d-123">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-123">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="0bf1d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bf1d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0bf1d-125">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-125">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0bf1d-126">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="0bf1d-126">-SkipStorage</span></span>
<span data-ttu-id="0bf1d-127">Gibt an, dass dieses Cmdlet die Konfiguration des Speichers überspringt.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-127">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf1d-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="0bf1d-128">-VMName</span></span>
<span data-ttu-id="0bf1d-129">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-129">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0bf1d-130">Mit diesem Cmdlet wird die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-130">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0bf1d-131">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0bf1d-131">-WADStorageAccountName</span></span>
<span data-ttu-id="0bf1d-132">Gibt den Namen des speicherkontos an, das dieses Cmdlet zum Konfigurieren der LinuxDiagnostics-oder IaaSDiagnostics-Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-132">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="0bf1d-133">Wenn auf dem virtuellen Computer kein Standardspeicher Konto verwendet wird, müssen Sie einen Wert für diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-133">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf1d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf1d-134">CommonParameters</span></span>
<span data-ttu-id="0bf1d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf1d-136">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bf1d-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf1d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0bf1d-137">INPUTS</span></span>

### <span data-ttu-id="0bf1d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0bf1d-138">System.String</span></span>

## <span data-ttu-id="0bf1d-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0bf1d-139">OUTPUTS</span></span>

### <span data-ttu-id="0bf1d-140">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0bf1d-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0bf1d-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="0bf1d-141">NOTES</span></span>

## <span data-ttu-id="0bf1d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0bf1d-142">RELATED LINKS</span></span>

[<span data-ttu-id="0bf1d-143">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0bf1d-143">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="0bf1d-144">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0bf1d-144">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="0bf1d-145">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0bf1d-145">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)



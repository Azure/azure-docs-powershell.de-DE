---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: 931ed484850654ecebc368ced0b378ce2a40944f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477246"
---
# <span data-ttu-id="9b6af-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9b6af-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="9b6af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b6af-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6af-103">Ermöglicht die Unterstützung für die Überwachung von SAP-Systemen.</span><span class="sxs-lookup"><span data-stu-id="9b6af-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b6af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b6af-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b6af-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b6af-105">DESCRIPTION</span></span>
<span data-ttu-id="9b6af-106">Das Cmdlet " **Satz-AzureRmVMAEMExtension** " aktualisiert die Konfiguration einer virtuellen Maschine, um die Unterstützung für die Überwachung von SAP-Systemen zu aktivieren oder zu aktualisieren, die auf dem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="9b6af-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="9b6af-107">Das Cmdlet installiert die Erweiterung Azure Enhanced Monitoring (AEM), die die Leistungsdaten erfasst und für das SAP-System auffindbar macht.</span><span class="sxs-lookup"><span data-stu-id="9b6af-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="9b6af-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b6af-108">EXAMPLES</span></span>

### <span data-ttu-id="9b6af-109">Beispiel 1: Verwenden der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="9b6af-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="9b6af-110">Dieser Befehl konfiguriert den virtuellen Computer mit dem Namen "Contoso-Server", um die AEM-Erweiterung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b6af-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="9b6af-111">Der Befehl gibt das Speicherkonto mit dem Namen "stdstorage" an.</span><span class="sxs-lookup"><span data-stu-id="9b6af-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="9b6af-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b6af-112">PARAMETERS</span></span>

### <span data-ttu-id="9b6af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6af-113">-DefaultProfile</span></span>
<span data-ttu-id="9b6af-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b6af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b6af-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="9b6af-115">-DisableWAD</span></span>
<span data-ttu-id="9b6af-116">Gibt an, dass dieses Cmdlet keine Azure-Diagnose für den virtuellen Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9b6af-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="9b6af-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="9b6af-117">-EnableWAD</span></span>
<span data-ttu-id="9b6af-118">Wenn dieser Parameter bereitgestellt wird, aktiviert der Unifiedgroup Windows Azure-Diagnose für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9b6af-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="9b6af-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="9b6af-119">-OSType</span></span>
<span data-ttu-id="9b6af-120">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="9b6af-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="9b6af-121">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="9b6af-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="9b6af-122">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="9b6af-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="9b6af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6af-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b6af-124">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9b6af-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9b6af-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="9b6af-125">-SkipStorage</span></span>
<span data-ttu-id="9b6af-126">Gibt an, dass dieses Cmdlet die Konfiguration des Speichers überspringt.</span><span class="sxs-lookup"><span data-stu-id="9b6af-126">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="9b6af-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="9b6af-127">-VMName</span></span>
<span data-ttu-id="9b6af-128">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="9b6af-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9b6af-129">Mit diesem Cmdlet wird die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9b6af-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b6af-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9b6af-130">-WADStorageAccountName</span></span>
<span data-ttu-id="9b6af-131">Gibt den Namen des speicherkontos an, das dieses Cmdlet zum Konfigurieren der LinuxDiagnostics-oder IaaSDiagnostics-Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b6af-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="9b6af-132">Wenn auf dem virtuellen Computer kein Standardspeicher Konto verwendet wird, müssen Sie einen Wert für diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="9b6af-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="9b6af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6af-133">CommonParameters</span></span>
<span data-ttu-id="9b6af-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6af-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b6af-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6af-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b6af-136">INPUTS</span></span>

## <span data-ttu-id="9b6af-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b6af-137">OUTPUTS</span></span>

## <span data-ttu-id="9b6af-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b6af-138">NOTES</span></span>

## <span data-ttu-id="9b6af-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b6af-139">RELATED LINKS</span></span>

[<span data-ttu-id="9b6af-140">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9b6af-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="9b6af-141">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9b6af-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="9b6af-142">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9b6af-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)



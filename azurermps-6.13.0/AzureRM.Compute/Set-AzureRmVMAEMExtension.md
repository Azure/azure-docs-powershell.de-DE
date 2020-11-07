---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: c006c06d03e1f1c120ed62f38ea8b3e451d8fa21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664878"
---
# <span data-ttu-id="850ed-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="850ed-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="850ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="850ed-102">SYNOPSIS</span></span>
<span data-ttu-id="850ed-103">Ermöglicht die Unterstützung für die Überwachung von SAP-Systemen.</span><span class="sxs-lookup"><span data-stu-id="850ed-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="850ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="850ed-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="850ed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="850ed-105">DESCRIPTION</span></span>
<span data-ttu-id="850ed-106">Das Cmdlet " **Satz-AzureRmVMAEMExtension** " aktualisiert die Konfiguration einer virtuellen Maschine, um die Unterstützung für die Überwachung von SAP-Systemen zu aktivieren oder zu aktualisieren, die auf dem virtuellen Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="850ed-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="850ed-107">Das Cmdlet installiert die Erweiterung Azure Enhanced Monitoring (AEM), die die Leistungsdaten erfasst und für das SAP-System auffindbar macht.</span><span class="sxs-lookup"><span data-stu-id="850ed-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="850ed-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="850ed-108">EXAMPLES</span></span>

### <span data-ttu-id="850ed-109">Beispiel 1: Verwenden der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="850ed-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="850ed-110">Dieser Befehl konfiguriert den virtuellen Computer mit dem Namen "Contoso-Server", um die AEM-Erweiterung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="850ed-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="850ed-111">Der Befehl gibt das Speicherkonto mit dem Namen "stdstorage" an.</span><span class="sxs-lookup"><span data-stu-id="850ed-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="850ed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="850ed-112">PARAMETERS</span></span>

### <span data-ttu-id="850ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="850ed-113">-DefaultProfile</span></span>
<span data-ttu-id="850ed-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="850ed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="850ed-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="850ed-115">-EnableWAD</span></span>
<span data-ttu-id="850ed-116">Wenn dieser Parameter bereitgestellt wird, aktiviert der Unifiedgroup Windows Azure-Diagnose für diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="850ed-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="850ed-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="850ed-117">-OSType</span></span>
<span data-ttu-id="850ed-118">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="850ed-118">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="850ed-119">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="850ed-119">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="850ed-120">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="850ed-120">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="850ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="850ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="850ed-122">Gibt den Namen der Ressourcengruppe des virtuellen Computers an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="850ed-122">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="850ed-123">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="850ed-123">-SkipStorage</span></span>
<span data-ttu-id="850ed-124">Gibt an, dass dieses Cmdlet die Konfiguration des Speichers überspringt.</span><span class="sxs-lookup"><span data-stu-id="850ed-124">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="850ed-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="850ed-125">-VMName</span></span>
<span data-ttu-id="850ed-126">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="850ed-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="850ed-127">Mit diesem Cmdlet wird die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="850ed-127">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="850ed-128">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="850ed-128">-WADStorageAccountName</span></span>
<span data-ttu-id="850ed-129">Gibt den Namen des speicherkontos an, das dieses Cmdlet zum Konfigurieren der LinuxDiagnostics-oder IaaSDiagnostics-Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="850ed-129">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="850ed-130">Wenn auf dem virtuellen Computer kein Standardspeicher Konto verwendet wird, müssen Sie einen Wert für diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="850ed-130">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="850ed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="850ed-131">CommonParameters</span></span>
<span data-ttu-id="850ed-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="850ed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="850ed-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="850ed-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="850ed-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="850ed-134">INPUTS</span></span>

### <span data-ttu-id="850ed-135">System. String</span><span class="sxs-lookup"><span data-stu-id="850ed-135">System.String</span></span>

## <span data-ttu-id="850ed-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="850ed-136">OUTPUTS</span></span>

### <span data-ttu-id="850ed-137">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="850ed-137">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="850ed-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="850ed-138">NOTES</span></span>

## <span data-ttu-id="850ed-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="850ed-139">RELATED LINKS</span></span>

[<span data-ttu-id="850ed-140">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="850ed-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="850ed-141">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="850ed-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="850ed-142">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="850ed-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)



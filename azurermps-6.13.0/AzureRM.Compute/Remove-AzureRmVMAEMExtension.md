---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: 96f9a3195747aff8d31261b7a6ae992a00adb82b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477901"
---
# <span data-ttu-id="29069-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="29069-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="29069-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29069-102">SYNOPSIS</span></span>
<span data-ttu-id="29069-103">Entfernt die AEM-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="29069-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29069-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29069-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29069-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29069-105">DESCRIPTION</span></span>
<span data-ttu-id="29069-106">Das Cmdlet **Remove-AzureRmVMAEMExtension** entfernt die Erweiterung Azure Enhanced Monitoring (AEM) von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="29069-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="29069-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29069-107">EXAMPLES</span></span>

### <span data-ttu-id="29069-108">Beispiel 1: Entfernen der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="29069-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="29069-109">Dieser Befehl entfernt die AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="29069-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="29069-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="29069-110">PARAMETERS</span></span>

### <span data-ttu-id="29069-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29069-111">-DefaultProfile</span></span>
<span data-ttu-id="29069-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29069-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29069-113">-Name</span><span class="sxs-lookup"><span data-stu-id="29069-113">-Name</span></span>
<span data-ttu-id="29069-114">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die AEM-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="29069-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="29069-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="29069-115">-OSType</span></span>
<span data-ttu-id="29069-116">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="29069-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="29069-117">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="29069-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="29069-118">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="29069-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="29069-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29069-119">-ResourceGroupName</span></span>
<span data-ttu-id="29069-120">Gibt den Namen der Ressourcengruppe einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="29069-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="29069-121">Dieses Cmdlet entfernt die AEM-Erweiterung von dieser virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="29069-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="29069-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="29069-122">-VMName</span></span>
<span data-ttu-id="29069-123">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="29069-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="29069-124">Dieses Cmdlet entfernt die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="29069-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="29069-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29069-125">CommonParameters</span></span>
<span data-ttu-id="29069-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29069-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29069-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29069-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29069-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29069-128">INPUTS</span></span>

### <span data-ttu-id="29069-129">System. String</span><span class="sxs-lookup"><span data-stu-id="29069-129">System.String</span></span>

## <span data-ttu-id="29069-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29069-130">OUTPUTS</span></span>

### <span data-ttu-id="29069-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="29069-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="29069-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="29069-132">NOTES</span></span>

## <span data-ttu-id="29069-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29069-133">RELATED LINKS</span></span>

[<span data-ttu-id="29069-134">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="29069-134">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="29069-135">Satz-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="29069-135">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="29069-136">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="29069-136">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)



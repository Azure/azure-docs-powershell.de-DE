---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 6e3803b7627e16a96c8101f3a6dd1eee5a1b2689
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844359"
---
# <span data-ttu-id="1be6e-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1be6e-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="1be6e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1be6e-102">SYNOPSIS</span></span>
<span data-ttu-id="1be6e-103">Entfernt eine SQL Server-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1be6e-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="1be6e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1be6e-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1be6e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1be6e-105">DESCRIPTION</span></span>
<span data-ttu-id="1be6e-106">Mit dem Cmdlet **Remove-AzVMSqlServerExtension** wird eine AzureSQL-Server Erweiterung von einem virtuellen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="1be6e-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="1be6e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1be6e-107">EXAMPLES</span></span>

### <span data-ttu-id="1be6e-108">Beispiel 1: Entfernen einer SQL Server-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="1be6e-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="1be6e-109">Dieser Befehl entfernt eine SQL Server-Erweiterung vom virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="1be6e-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="1be6e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1be6e-110">PARAMETERS</span></span>

### <span data-ttu-id="1be6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be6e-111">-DefaultProfile</span></span>
<span data-ttu-id="1be6e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1be6e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be6e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1be6e-113">-Name</span></span>
<span data-ttu-id="1be6e-114">Gibt den Namen der SQL Server-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1be6e-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be6e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1be6e-115">-ResourceGroupName</span></span>
<span data-ttu-id="1be6e-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1be6e-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be6e-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="1be6e-117">-VMName</span></span>
<span data-ttu-id="1be6e-118">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die SQL Server-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="1be6e-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be6e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be6e-119">CommonParameters</span></span>
<span data-ttu-id="1be6e-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be6e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be6e-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1be6e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be6e-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1be6e-122">INPUTS</span></span>

### <span data-ttu-id="1be6e-123">Keine</span><span class="sxs-lookup"><span data-stu-id="1be6e-123">None</span></span>
<span data-ttu-id="1be6e-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1be6e-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1be6e-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1be6e-125">OUTPUTS</span></span>

### <span data-ttu-id="1be6e-126">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1be6e-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1be6e-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="1be6e-127">NOTES</span></span>

## <span data-ttu-id="1be6e-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1be6e-128">RELATED LINKS</span></span>

[<span data-ttu-id="1be6e-129">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1be6e-129">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="1be6e-130">Satz-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1be6e-130">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)



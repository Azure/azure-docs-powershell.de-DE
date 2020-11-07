---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: aa37745469ad6610fa2511d49c3404bbf54d8059
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850095"
---
# <span data-ttu-id="fb834-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fb834-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="fb834-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb834-102">SYNOPSIS</span></span>
<span data-ttu-id="fb834-103">Entfernt eine SQL Server-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="fb834-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb834-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb834-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb834-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb834-105">DESCRIPTION</span></span>
<span data-ttu-id="fb834-106">Mit dem Cmdlet **Remove-AzureRmVMSqlServerExtension** wird eine AzureSQL-Server Erweiterung von einem virtuellen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb834-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="fb834-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb834-107">EXAMPLES</span></span>

### <span data-ttu-id="fb834-108">Beispiel 1: Entfernen einer SQL Server-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="fb834-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="fb834-109">Dieser Befehl entfernt eine SQL Server-Erweiterung vom virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="fb834-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="fb834-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb834-110">PARAMETERS</span></span>

### <span data-ttu-id="fb834-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb834-111">-DefaultProfile</span></span>
<span data-ttu-id="fb834-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb834-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb834-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fb834-113">-Name</span></span>
<span data-ttu-id="fb834-114">Gibt den Namen der SQL Server-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="fb834-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fb834-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb834-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb834-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="fb834-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fb834-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="fb834-117">-VMName</span></span>
<span data-ttu-id="fb834-118">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die SQL Server-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb834-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="fb834-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb834-119">CommonParameters</span></span>
<span data-ttu-id="fb834-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb834-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb834-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb834-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb834-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb834-122">INPUTS</span></span>

### <span data-ttu-id="fb834-123">Keine</span><span class="sxs-lookup"><span data-stu-id="fb834-123">None</span></span>
<span data-ttu-id="fb834-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fb834-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb834-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb834-125">OUTPUTS</span></span>

### <span data-ttu-id="fb834-126">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fb834-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fb834-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb834-127">NOTES</span></span>

## <span data-ttu-id="fb834-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb834-128">RELATED LINKS</span></span>

[<span data-ttu-id="fb834-129">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fb834-129">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="fb834-130">Satz-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fb834-130">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



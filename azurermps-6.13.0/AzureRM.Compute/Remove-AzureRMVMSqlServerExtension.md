---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 83f697733d56ae7d99bc0b2660b5abbaca15a71f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504490"
---
# <span data-ttu-id="c3197-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c3197-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="c3197-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3197-102">SYNOPSIS</span></span>
<span data-ttu-id="c3197-103">Entfernt eine SQL Server-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c3197-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3197-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3197-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3197-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3197-105">DESCRIPTION</span></span>
<span data-ttu-id="c3197-106">Mit dem Cmdlet **Remove-AzureRmVMSqlServerExtension** wird eine AzureSQL-Server Erweiterung von einem virtuellen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="c3197-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="c3197-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3197-107">EXAMPLES</span></span>

### <span data-ttu-id="c3197-108">Beispiel 1: Entfernen einer SQL Server-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="c3197-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="c3197-109">Dieser Befehl entfernt eine SQL Server-Erweiterung vom virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="c3197-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="c3197-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3197-110">PARAMETERS</span></span>

### <span data-ttu-id="c3197-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3197-111">-DefaultProfile</span></span>
<span data-ttu-id="c3197-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3197-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3197-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c3197-113">-Name</span></span>
<span data-ttu-id="c3197-114">Gibt den Namen der SQL Server-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c3197-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3197-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3197-115">-ResourceGroupName</span></span>
<span data-ttu-id="c3197-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="c3197-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c3197-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="c3197-117">-VMName</span></span>
<span data-ttu-id="c3197-118">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die SQL Server-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="c3197-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="c3197-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3197-119">CommonParameters</span></span>
<span data-ttu-id="c3197-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3197-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3197-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3197-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3197-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3197-122">INPUTS</span></span>

### <span data-ttu-id="c3197-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c3197-123">System.String</span></span>

## <span data-ttu-id="c3197-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3197-124">OUTPUTS</span></span>

### <span data-ttu-id="c3197-125">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c3197-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c3197-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3197-126">NOTES</span></span>

## <span data-ttu-id="c3197-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3197-127">RELATED LINKS</span></span>

[<span data-ttu-id="c3197-128">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c3197-128">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="c3197-129">Satz-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c3197-129">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: f074d61919098d6c23ab39424774d9ba18e457d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478597"
---
# <span data-ttu-id="05036-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="05036-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="05036-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05036-102">SYNOPSIS</span></span>
<span data-ttu-id="05036-103">Entfernt eine SQL Server-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="05036-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05036-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05036-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="05036-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05036-105">DESCRIPTION</span></span>
<span data-ttu-id="05036-106">Mit dem Cmdlet **Remove-AzureRmVMSqlServerExtension** wird eine AzureSQL-Server Erweiterung von einem virtuellen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="05036-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="05036-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05036-107">EXAMPLES</span></span>

### <span data-ttu-id="05036-108">Beispiel 1: Entfernen einer SQL Server-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="05036-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="05036-109">Dieser Befehl entfernt eine SQL Server-Erweiterung vom virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="05036-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="05036-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="05036-110">PARAMETERS</span></span>

### <span data-ttu-id="05036-111">-Name</span><span class="sxs-lookup"><span data-stu-id="05036-111">-Name</span></span>
<span data-ttu-id="05036-112">Gibt den Namen der SQL Server-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="05036-112">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="05036-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05036-113">-ResourceGroupName</span></span>
<span data-ttu-id="05036-114">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="05036-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="05036-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="05036-115">-VMName</span></span>
<span data-ttu-id="05036-116">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die SQL Server-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="05036-116">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="05036-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05036-117">CommonParameters</span></span>
<span data-ttu-id="05036-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05036-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05036-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05036-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05036-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05036-120">INPUTS</span></span>

### <span data-ttu-id="05036-121">Keine</span><span class="sxs-lookup"><span data-stu-id="05036-121">None</span></span>
<span data-ttu-id="05036-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="05036-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05036-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05036-123">OUTPUTS</span></span>

## <span data-ttu-id="05036-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="05036-124">NOTES</span></span>

## <span data-ttu-id="05036-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05036-125">RELATED LINKS</span></span>

[<span data-ttu-id="05036-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="05036-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="05036-127">Satz-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="05036-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



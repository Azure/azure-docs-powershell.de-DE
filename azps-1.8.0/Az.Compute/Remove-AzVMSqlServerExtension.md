---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 630df5bbe6677c7019d372a2a6977cc4c724a421
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661480"
---
# <span data-ttu-id="81909-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="81909-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="81909-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81909-102">SYNOPSIS</span></span>
<span data-ttu-id="81909-103">Entfernt eine SQL Server-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="81909-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="81909-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81909-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81909-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81909-105">DESCRIPTION</span></span>
<span data-ttu-id="81909-106">Mit dem Cmdlet **Remove-AzVMSqlServerExtension** wird eine AzureSQL-Server Erweiterung von einem virtuellen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="81909-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="81909-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81909-107">EXAMPLES</span></span>

### <span data-ttu-id="81909-108">Beispiel 1: Entfernen einer SQL Server-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="81909-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="81909-109">Dieser Befehl entfernt eine SQL Server-Erweiterung vom virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="81909-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="81909-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="81909-110">PARAMETERS</span></span>

### <span data-ttu-id="81909-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81909-111">-DefaultProfile</span></span>
<span data-ttu-id="81909-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81909-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81909-113">-Name</span><span class="sxs-lookup"><span data-stu-id="81909-113">-Name</span></span>
<span data-ttu-id="81909-114">Gibt den Namen der SQL Server-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="81909-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="81909-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81909-115">-ResourceGroupName</span></span>
<span data-ttu-id="81909-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="81909-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="81909-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="81909-117">-VMName</span></span>
<span data-ttu-id="81909-118">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die SQL Server-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="81909-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="81909-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81909-119">CommonParameters</span></span>
<span data-ttu-id="81909-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81909-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81909-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81909-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81909-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81909-122">INPUTS</span></span>

### <span data-ttu-id="81909-123">System. String</span><span class="sxs-lookup"><span data-stu-id="81909-123">System.String</span></span>

## <span data-ttu-id="81909-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81909-124">OUTPUTS</span></span>

### <span data-ttu-id="81909-125">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="81909-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="81909-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="81909-126">NOTES</span></span>

## <span data-ttu-id="81909-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81909-127">RELATED LINKS</span></span>

[<span data-ttu-id="81909-128">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="81909-128">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="81909-129">Satz-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="81909-129">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)



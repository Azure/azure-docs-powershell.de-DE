---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472998"
---
# <span data-ttu-id="37a76-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="37a76-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="37a76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37a76-102">SYNOPSIS</span></span>
<span data-ttu-id="37a76-103">Entfernt eine SQL Server Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="37a76-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="37a76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37a76-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37a76-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37a76-105">DESCRIPTION</span></span>
<span data-ttu-id="37a76-106">Das **Cmdlet "Remove-AzVMSqlServerExtension"** entfernt eine AzureSQL -Server-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="37a76-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="37a76-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37a76-107">EXAMPLES</span></span>

### <span data-ttu-id="37a76-108">Beispiel 1: Entfernen SQL Server Erweiterung</span><span class="sxs-lookup"><span data-stu-id="37a76-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="37a76-109">Mit diesem Befehl wird eine SQL Server vom virtuellen Computer "ContosoVM22" entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a76-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="37a76-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37a76-110">PARAMETERS</span></span>

### <span data-ttu-id="37a76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a76-111">-DefaultProfile</span></span>
<span data-ttu-id="37a76-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37a76-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37a76-113">-Name</span><span class="sxs-lookup"><span data-stu-id="37a76-113">-Name</span></span>
<span data-ttu-id="37a76-114">Gibt den Namen der SQL Server erweiterung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="37a76-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="37a76-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="37a76-115">-NoWait</span></span>
<span data-ttu-id="37a76-116">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="37a76-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="37a76-117">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="37a76-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="37a76-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a76-118">-ResourceGroupName</span></span>
<span data-ttu-id="37a76-119">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="37a76-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="37a76-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="37a76-120">-VMName</span></span>
<span data-ttu-id="37a76-121">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die SQL Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="37a76-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="37a76-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a76-122">CommonParameters</span></span>
<span data-ttu-id="37a76-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a76-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a76-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37a76-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a76-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37a76-125">INPUTS</span></span>

### <span data-ttu-id="37a76-126">System.String</span><span class="sxs-lookup"><span data-stu-id="37a76-126">System.String</span></span>

## <span data-ttu-id="37a76-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37a76-127">OUTPUTS</span></span>

### <span data-ttu-id="37a76-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="37a76-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="37a76-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37a76-129">NOTES</span></span>

## <span data-ttu-id="37a76-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37a76-130">RELATED LINKS</span></span>

[<span data-ttu-id="37a76-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="37a76-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="37a76-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="37a76-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)



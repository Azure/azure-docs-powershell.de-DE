---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173311"
---
# <span data-ttu-id="d55ec-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d55ec-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="d55ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d55ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d55ec-103">Entfernt eine SQL Server-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d55ec-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="d55ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d55ec-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d55ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d55ec-105">DESCRIPTION</span></span>
<span data-ttu-id="d55ec-106">Mit dem Cmdlet **Remove-AzVMSqlServerExtension** wird eine AzureSQL-Server Erweiterung von einem virtuellen Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="d55ec-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="d55ec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d55ec-107">EXAMPLES</span></span>

### <span data-ttu-id="d55ec-108">Beispiel 1: Entfernen einer SQL Server-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="d55ec-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="d55ec-109">Dieser Befehl entfernt eine SQL Server-Erweiterung vom virtuellen Computer mit dem Namen ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="d55ec-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="d55ec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d55ec-110">PARAMETERS</span></span>

### <span data-ttu-id="d55ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55ec-111">-DefaultProfile</span></span>
<span data-ttu-id="d55ec-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d55ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d55ec-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d55ec-113">-Name</span></span>
<span data-ttu-id="d55ec-114">Gibt den Namen der SQL Server-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d55ec-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d55ec-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d55ec-115">-NoWait</span></span>
<span data-ttu-id="d55ec-116">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="d55ec-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d55ec-117">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d55ec-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d55ec-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d55ec-118">-ResourceGroupName</span></span>
<span data-ttu-id="d55ec-119">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d55ec-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d55ec-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="d55ec-120">-VMName</span></span>
<span data-ttu-id="d55ec-121">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die SQL Server-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="d55ec-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="d55ec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55ec-122">CommonParameters</span></span>
<span data-ttu-id="d55ec-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d55ec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55ec-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d55ec-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55ec-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d55ec-125">INPUTS</span></span>

### <span data-ttu-id="d55ec-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d55ec-126">System.String</span></span>

## <span data-ttu-id="d55ec-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d55ec-127">OUTPUTS</span></span>

### <span data-ttu-id="d55ec-128">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d55ec-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d55ec-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="d55ec-129">NOTES</span></span>

## <span data-ttu-id="d55ec-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d55ec-130">RELATED LINKS</span></span>

[<span data-ttu-id="d55ec-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d55ec-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="d55ec-132">Satz-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d55ec-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)



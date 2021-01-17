---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363948"
---
# <span data-ttu-id="70079-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="70079-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="70079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70079-102">SYNOPSIS</span></span>

<span data-ttu-id="70079-103">Ruft eine Liste der Wiederherstellungsdienste-Tresore ab.</span><span class="sxs-lookup"><span data-stu-id="70079-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="70079-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70079-104">SYNTAX</span></span>

### <span data-ttu-id="70079-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="70079-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70079-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70079-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70079-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70079-107">DESCRIPTION</span></span>

<span data-ttu-id="70079-108">Das **Cmdlet "Get-AzRecoveryServicesVault"** ruft eine Liste der Recovery Services-Tresore im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="70079-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="70079-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70079-109">EXAMPLES</span></span>

### <span data-ttu-id="70079-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70079-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="70079-111">Holen Sie sich die Liste des Tresors im ausgewählten Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70079-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="70079-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="70079-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="70079-113">Holen Sie sich die Liste des Tresors in der Ressourcengruppe im ausgewählten Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70079-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="70079-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="70079-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="70079-115">Holen Sie sich den Tresor in der Ressourcengruppe mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="70079-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="70079-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70079-116">PARAMETERS</span></span>

### <span data-ttu-id="70079-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70079-117">-DefaultProfile</span></span>

<span data-ttu-id="70079-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70079-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70079-119">-Name</span><span class="sxs-lookup"><span data-stu-id="70079-119">-Name</span></span>

<span data-ttu-id="70079-120">Gibt den Namen des Tresors an, nach dem eine Abfrage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="70079-120">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="70079-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70079-121">-ResourceGroupName</span></span>

<span data-ttu-id="70079-122">Gibt den Namen der Azure-Ressourcengruppe an, aus der das angegebene Wiederherstellungsdienstobjekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="70079-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70079-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="70079-123">-Tag</span></span>

<span data-ttu-id="70079-124">Gibt die Tags an, die abgefragt werden müssen</span><span class="sxs-lookup"><span data-stu-id="70079-124">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70079-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="70079-125">-TagName</span></span>

<span data-ttu-id="70079-126">Gibt den Schlüssel des tags an, für den eine Abfrage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="70079-126">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70079-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="70079-127">-TagValue</span></span>

<span data-ttu-id="70079-128">Gibt den Wert des Tags an, für das eine Abfrage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="70079-128">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70079-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70079-129">CommonParameters</span></span>
<span data-ttu-id="70079-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70079-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70079-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70079-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70079-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70079-132">INPUTS</span></span>

### <span data-ttu-id="70079-133">Keine</span><span class="sxs-lookup"><span data-stu-id="70079-133">None</span></span>

## <span data-ttu-id="70079-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70079-134">OUTPUTS</span></span>

### <span data-ttu-id="70079-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="70079-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="70079-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70079-136">NOTES</span></span>
<span data-ttu-id="70079-137">Get-AzRecoveryServicesVault in der alten Version von Az.RecoveryServices(<=2.10.0) kann mit Az.Accounts(>=1.8.1) aufgrund eines falschen Assemblyverweises nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70079-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="70079-138">Das Modul Az.RecoveryServices muss auf 2.11.0 oder neuer aktualisiert werden, wenn Sie die neuesten Az- oder Az.-Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="70079-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="70079-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70079-139">RELATED LINKS</span></span>

[<span data-ttu-id="70079-140">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="70079-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="70079-141">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="70079-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="70079-142">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="70079-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
